# Papertrail CLI #

I add this to a sourced bash file (works in ZSH too).

    papertrail-cli() {
        docker run -e PAPERTRAIL_API_TOKEN=${PAPERTRAIL_API_TOKEN} --rm gvangool/papertrail-cli $@
    }

    # Add coloring again
    pt() {
        papertrail-cli $@ | perl -pe 's/^(.{15})(.)([\S]+)(.)([\S]+)/\e[1;32m\1\e[0m\2\e[34m\3\e[0m\4\e[36m\5\e[0m/g'
    }


So now you can just use this:

    pt -f
    pt -f -- "-collectd -dhcp -NetworkManager"
    pf -f -s my-fancy-server
