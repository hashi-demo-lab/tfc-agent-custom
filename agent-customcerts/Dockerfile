FROM --platform=linux/amd64 hashicorp/tfc-agent:latest

USER root

ADD ./tfe_root.crt /usr/local/share/ca-certificates/tfe_root.crt
ADD ./tfe-no-root.crt /usr/local/share/ca-certificates/tfe-no-root.crt
RUN chmod 644 /usr/local/share/ca-certificates/tfe_root.crt /usr/local/share/ca-certificates/tfe-no-root.crt && update-ca-certificates

USER tfc-agent