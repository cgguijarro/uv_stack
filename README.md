# uv_stack
Script for uv-stacking in two versions: without weighting and with a weighting based on a 1.1mm flux normalization.

What the script does is to take a list of sources RA, Dec that you want to stack. Then, it searches for the pointings that contain those coordinates. Phase-shift each coordinate to put them at the phase center modulo a primary beam correction (which assumes the source is small enough so a single primary beam correction for each source is applicable). Once all the pointings are phase-shifted it concatenates them into a single MS file modulo some needed commands to make sure the previous thing works and the weights of the different visibilities are correct.

In order to use the script it is very straighforward and self-explanatory, you just need to introduce (see the script for an example):

- Path to where the individual pointings and associated primary beams are located
- List of IDs (string)
- List of RA (float)
- List of Dec (float)
- List of RA, Dec coordinates (string) preceded by J2000 and in hh:mm:ss dd:mm:ss
- (if flux normalization weights applied) list of fluxes (float)
