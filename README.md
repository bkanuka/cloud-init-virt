# cloud-init-virt

## How-to:

  1. Clone this repository:

  ```bash
  git clone https://github.com/bkanuka/cloud-init-virt.git
  ```
  1. Go to http://cloud-images.ubuntu.com/trusty/current/ and download the image of choice. Most likely this can be accomplished using:

  ```bash
  wget http://cloud-images.ubuntu.com/trusty/current/trusty-server-cloudimg-amd64-disk1.img
  ```
  1. Copy `config.sample` to `config`:

  ```bash
  cp config.sample config
  ```
  2. Edit `config` to set the Hostname and some other things.
  3. Edit `user-data` to your liking. Unfortunately I have not found any good guides for this. I've collected some things from http://cloudinit.readthedocs.org/en/latest/topics/examples.html
  4. Run `./install`
  5. If finished, `./destroy [hostname]` will completely remove the VM including storage.
