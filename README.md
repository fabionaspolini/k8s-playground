kubectl \
    run fabio-temp-net-utils \
    -i --tty --rm --restart=Never \
    --namespace teste \
    --image=fabionaspolini/net-utils \
    --image-pull-policy=Always \
    -- \
    bash