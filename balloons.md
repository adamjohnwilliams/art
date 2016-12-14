# BALLOONS
## adam john williams 2016

balloons is an 888-byte digital artwork consisting of a poem about the experience of ego death whilst under the influence of nitrous oxide/"laughing gas"

the poem is followed by sonic pi code which produces generative music to accompany the poem, processed with effects to simulate the auditory hallucinations caused by the nitrous oxide

its size is limited to 888 bytes so that it can be stored on an ntag216 NFC/RFID chip which has been implanted into the artist's left hand

poem & code reproduced below, or download from https://adamjohnwilliams.github.io/art/balloons

use sonic pi to hear & interact with the music https://github.com/samaaron/sonic-pi

performance video coming soon

<img src="https://adamjohnwilliams.github.io/art/adamjohnwilliams_balloons.jpg" width="800" alt text="hand of the artist - NFC chip can be seen between thumb & forefinger">

`#And what if when, I turn to dust
#The earth collapses in around me
#Falling, shrinking down, compressing
#Passing to the other side

#And in that moment, movement ceases
#All is still, no time progresses
#Curtain up, expose the mechanism
#Hey, remember the balloons?
live_loop :k do
sample :bd_haus
sleep 0.5
sample :bd_haus
sample :sn_dolf, amp: 0
sleep 0.5
end
live_loop :h do
sleep 0.25
sample :drum_cymbal_closed, amp: 0
sleep 0.25
end
live_loop :b do
sample :bass_hit_c, rate: 1, amp: 0.7, cutoff: (rrand_i 30, 80), res: 0.8
sleep 0.25
end
with_fx :slicer do
with_fx :ixi_techno do
with_fx :reverb do
live_loop :nos do
sample :ambi_drone, rate: 1
2.times do
sample :ambi_choir, rate: (rrand 0.12, 1.5), amp: 0
sleep 0.25
end
4.times do
sample :perc_bell, rate: (rrand 0.12, 1.5), amp: 0
sleep rrand(0.2, 2)
end
end
end
end
end
#use Sonic Pi, change amp val
#Adam John Williams 2016`
