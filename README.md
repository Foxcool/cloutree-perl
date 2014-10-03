# WWW::Cloutree
[![Build Status](https://travis-ci.org/IvanShamatov/cloutree.png?branch=master)](https://travis-ci.org/IvanShamatov/cloutree)

Perl module to upload files to Cloutr.ee CDN

Installing

    $ cpanm install WWW::Cloutree

    or

    $ cpan install WWW::Cloutree  

## Usage

    use WWW::Cloutree;
    my $cloutree = WWW::Cloutree->instance( {
      app_key => 'YOUR_APP_KEY',
      app_secret => 'YOUR_APP_SECRET'
    } );
    my $result = $cloutree->upload_file({
      file => $opts{file},
      filename => 'filename'
    });
    say $result->{success}; # say link of uploaded file
