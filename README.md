# imagemaster3000

Downloads and slightly modifies cloud images so they can be used in our extraordinary cloud. Simple as that.

## Installation

### From source (dev)
**Installation from source should never be your first choice! Especially, if you are not
familiar with RVM, Bundler, Rake and other dev tools for Ruby!**

**However, if you wish to contribute to our project, this is the right way to start.**

To build and install the bleeding edge version from master

```bash
git clone git://github.com/Misenko/imagemaster3000.git
cd imagemaster3000
gem install bundler
bundle install
bundle exec rake spec
```

## Usage
```
Usage:
  imagemaster3000 start --binaries-guestfish=BINARIES-GUESTFISH --binaries-virt-copy-in=BINARIES-VIRT-COPY-IN --certificate=CERTIFICATE --definitions-repository=DEFINITIONS-REPOSITORY --endpoint=ENDPOINT --group=GROUP
--image-dir=IMAGE-DIR --image-list-description=IMAGE-LIST-DESCRIPTION --image-list-identifier=IMAGE-LIST-IDENTIFIER --image-list-mpuri=IMAGE-LIST-MPURI --image-list-path=IMAGE-LIST-PATH --image-list-source=IMAGE-LIST-S
OURCE --key=KEY

Options:
  --definitions-repository=DEFINITIONS-REPOSITORY  # Repository from which image definitions will be downloaded
  [--definitions-branch=DEFINITIONS-BRANCH]        # Repository branch that will be used
  --image-dir=IMAGE-DIR                            # Directory where to temporarily store images
                                                   # Default: /var/spool/imagemaster3000/
  --group=GROUP                                    # Group, images will be uploaded to
                                                   # Default: imagemaster3000
  --image-list-path=IMAGE-LIST-PATH                # Name and path of generated image list
                                                   # Default: /var/spool/imagemaster3000/imagemaster3000.list
  --image-list-description=IMAGE-LIST-DESCRIPTION  # Imagelist description required by cloudkeeper
                                                   # Default: Imagemaster3000 image list
  --image-list-identifier=IMAGE-LIST-IDENTIFIER    # Imagelist identifier required by cloudkeeper
                                                   # Default: Imagemaster3000 cloud images
  --image-list-source=IMAGE-LIST-SOURCE            # Imagelist source required by cloudkeeper
                                                   # Default: https://cloud.metacentrum.cz/
  --image-list-mpuri=IMAGE-LIST-MPURI              # Imagelist mpuri required by cloudkeeper
                                                   # Default: mpuri-placeholder
  --endpoint=ENDPOINT                              # Endpoint where image list will be available
                                                   # Default: http://localhost/
  --certificate=CERTIFICATE                        # Certificate to sign image list with
                                                   # Default: /etc/grid-security/cert.pem
  --key=KEY                                        # Key to sign image list with
                                                   # Default: /etc/grid-security/key.pem
  --binaries-virt-copy-in=BINARIES-VIRT-COPY-IN    # Path to binary needed for 'copy' action
                                                   # Default: /usr/bin/virt-copy-in
  --binaries-guestfish=BINARIES-GUESTFISH          # Path to binary needed for 'remove' action
                                                   # Default: /usr/bin/guestfish
  --logging-level=LOGGING-LEVEL
                                                   # Default: ERROR
                                                   # Possible values: DEBUG, INFO, WARN, ERROR, FATAL, UNKNOWN
  [--logging-file=LOGGING-FILE]                    # File to write logs to
                                                   # Default: /var/log/imagemaster3000/imagemaster3000.log
  [--debug], [--no-debug]                          # Runs in debug mode
```

## Contributing
1. Fork it ( https://github.com/Misenko/imagemaster3000/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
