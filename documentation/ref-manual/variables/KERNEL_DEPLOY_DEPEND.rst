Provides a means of controlling the dependency of an image recipe
on the kernel. The default value is "virtual/kernel:do_deploy",
however for a small initramfs image or other images that do not
need the kernel, this can be set to "" in the image recipe.
