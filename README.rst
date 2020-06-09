Drawing patterns of seismicity -- Fluid/fault interplay in a subduction zone
============================================================================

This repo contains the code used to produce the animation I submitted to the
Scipy 2020 Excellence in plotting contest. Because the complete
data files are too big to be hosted here, only simplified data is provided,
downsampled at times corresponding to the animation frames.

Dependencies to run the notebook
--------------------------------

Nothing fancy here, the version numbers I use to run the notebook are specified in
between brackets, for reference:
- matplotlib (3.2.1)
- numpy (1.18.5)
- jupyter_contrib_nbextensions (only esthetic, for cell folding)

A word on the work this animation is an visualisation of
--------------------------------------------------------

Subduction zones like the ones ashore of Japan, Alaska or Chile produce the
largest earthquakes (up to magnitude 9), as an oceanic plate suddenly
slips down into the earth mantle, rubbing against the overriding plate.
They also produce a constant
chatter of much smaller and subtler earthquakes (below magnitude 2), providing 
an almost continuous flow of information on the state of stress that the subduction
interface is under, and ideally, on the chances of an earthquake happening.

The activity of these earthquakes draws swarm-like patterns: they buzz for a while and then die as fast as they emerged, intermittently, sometimes even periodically, migrating along the fault (1 km/day to 10 km/hr). The mechanism producing those patterns is not well understood. Unstable fluid flow within the subduction interface is suspected to drive the emergence, extinction and migrations of the earthquake swarms. This fluid is mostly composed of water and dissolved mineral elements coming from the dehydration of the subducting plate, as it dives into the ever hotter and denser Earth mantle. At 40 km depth, under high pressure (10 000 atmospheric pressure) and temperature (~ 500 K), the fluid is in a super-critical state.

Our work is an attempt to test if simple earthquake sources triggered by, and
communicating through fluid pressure in the subduction fault only could
reproduce the swarm-like patterns of activity we observe in the field.

We model fluid diffusion in a porous, linear channel on the fault interface
between plates. The throbbing blue band in the lower panel of the animation
shows the distribution of fluid in the channel as it diffuses. The larger the
band, the denser the fluid is packed at this location. The vertical stripes are earthquake sources along the fault channel, modeled as valves.  
When closed, they appear in gray, and block the flux. It causes fluid to
accumulate behind them and be depleted above, until the fluid pressure forces
them to brutally release it, triggering an earthquake, detected in the
top panel. They then close when the pressure comes back to base
levels, turning very dim, blocking the flux again.
The top panel represents what is actually recorded in the field, a
catalog of earthquake times and epicenters. 

As the animation plays, you will see how the system activates intermittently, periodically producing swarms of earthquakes. When time slows down, you can spot fast migrations of the seismic activity along the fault. This animation allows us to articulate how
the action unfolds behind the scenes. We see how fluid is densely packed at the
bottom and depleted at the top of the channel, and then released in a swarm of
events. We see how the fault channel zips closed and unzips as valves
break, drawing the patterns that we record at the surface.

The most simple models are often the furthest from how anyone sees of our
object of study and it makes it hard to represent them in a compelling way. We hope this animation can bridge this gap: representative both of the geological observations, and of the clockwork of the model.

Some references
---------------
Observations
^^^^^^^^^^^^
+ Frank, W. B., Shapiro, N. M., Husker, A. L., Kostoglodov, V., Romanenko, A., & Campillo, M. (2014). Using systematically characterized low-frequency earthquakes as a fault probe in Guerrero, Mexico: FRANK ET AL. Journal of Geophysical Research: Solid Earth, 119(10), 7686–7700. https://doi.org/10.1002/2014JB011457
+ Frank, W. B., Shapiro, N. M., Husker, A. L., Kostoglodov, V., Gusev, A. A., & Campillo, M. (2016). The evolving interaction of low-frequency earthquakes during transient slip. Science Advances, 2(4), e1501616. https://doi.org/10.1126/sciadv.1501616

Modeling fluid circulation and seismic activity
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
+ Shapiro, N. M., Campillo, M., Kaminski, E., Vilotte, J., & Jaupart, C. (2018). Low‐Frequency Earthquakes and Pore Pressure Transients in Subduction Zones. Geophysical Research Letters, 45(20). https://doi.org/10.1029/2018GL079893
