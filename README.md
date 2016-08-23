## Warning this is still work in progress

# MMM-voice
Voice Recognition Module for MagicMirror<sup>2</sup>

## Dependencies
  * An installation of [MagicMirror<sup>2</sup>](https://github.com/MichMich/MagicMirror)
  * Packages: bison libasound2-dev autoconf automake libtool python-dev swig python-pip
  * [SphinxBase](https://github.com/cmusphinx/sphinxbase)
  * [pocketsphinx](https://github.com/cmusphinx/pocketsphinx)
  * [cmuclmtk-0.7](https://sourceforge.net/projects/cmusphinx/files/cmuclmtk/0.7/)
  * [tensorflow](https://github.com/samjabrahams/tensorflow-on-raspberry-pi)
  * [g2p-seq2seq](https://github.com/cmusphinx/g2p-seq2seq)
  * A microphone
  * npm
  * [pocketsphinx-continuous](https://www.npmjs.com/package/pocketsphinx-continuous)

## Installation
 1. Clone this repo into `~/MagicMirror/modules` directory.
 2. Run command `bash dependencies.sh` in `~/MagicMirror/modules/MMM-voice/installers` directory, to install all dependencies. This will need a couple of minutes.
 3. Configure your `~/MagicMirror/config/config.js`:
 
     ```
     {
         module: 'MMM-voice',
         position: 'bottom_bar',
         config: {
             microphone: 1,
             ...
         }
     }
     ```

## Config Options
| **Option** | **Default** | **Description** |
| --- | --- | --- |
| `microphone` | REQUIRED | Id of microphone shown in the installer. |
| `keyword` | `'MAGIC MIRROR'` | Keyword the mirror starts to listen. |
| `timeout` | `15` | time the keyword should be active without saying something |

## Custom Dictionairy
Go to [Sphinx Knowledge Base Tool](http://www.speech.cs.cmu.edu/tools/lmtool-new.html) and create your own
