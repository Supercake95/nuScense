# nuScense
  modified plt.
 
  download nuscenes and place it to:

  /home/usrname/anaconda3/envs/yourenvname/lib/python3.6/site-packages/nuscenes 

so you can plot Radar Pointcloud to the image where is able to draw colors according to dimensions:

    from nuscenes.nuscenes import NuScenes
    nusc = NuScenes(version='v1.0-trainval', dataroot='/gruntdata3', verbose=True)

    my_sample = nusc.sample[19691]
    for i in range(0,18): 
      nusc.render_pointcloud_in_image(2,my_sample['token'], pointsensor_channel='RADAR_FRONT_RIGHT',camera_channel= 'CAM_FRONT_RIGHT')
