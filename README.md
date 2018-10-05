# sbx-metaphlan

[Sunbeam] extension for running [MetaPhlAn2], adapted from
[zhaoc1](https://github.com/zhaoc1)'s
[sunbeam_neutrino](https://github.com/PennChopMicrobiomeProgram/sunbeam_neutrino).

## Installation

    git clone https://github.com/ressy/sbx_metaphlan
    cat sunbeam/extensions/sbx_metaphlan/config.yml >> sunbeam_config.yml

## Running

This extension uses a [docker image] for MetaPhlAn2, so you need to include the `--use-singularity --singularity-args "-B /mnt/isilon/:/mnt/isilon/"` argument when running
Sunbeam:

    sunbeam run --configfile=sunbeam_config.yml --use-singularity --singularity-args "-B /mnt/isilon/:/mnt/isilon/" all_metaphlan

[Sunbeam]: https://github.com/sunbeam-labs/sunbeam
[MetaPhlAn2]: https://bitbucket.org/biobakery/metaphlan2
[docker image]: https://hub.docker.com/r/samesense/metaphlan2-docker/
