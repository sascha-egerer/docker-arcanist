# Arcanist docker image

A basic image containing arcanist.

The local .arcrc, .ssh and git config should be mounted to the container as
all the other stuff you need.

```
docker run --rm -it \
	-v ~/.arcrc:/home/www-data/.arcrc \
	-v ~/.gitconfig:/home/www-data/.gitconfig \
	-v ~/.ssh:/home/www-data/.ssh \
	-v $(pwd)/:/var/www/ \
	arcanist \
	arc list
```