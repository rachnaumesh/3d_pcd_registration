# 3d-pcd-registration

3d-pcd-registration: The process of aligning two or more 3-D point clouds of the same scene into a common coordinate system. Here, 3d point clouds are 3D datasets that represent objects or space. This assignment's aim is to understand your problem solving skills with 3d Data.

Problem statement 1: There are two point cloud files provided sync_1.ply and sync_2.ply (.ply 3D file format) and the task is to find the points that overlap. You can use open3d library to load .ply files and get the 3d point information and visualise.

Example:

import open3d as o3d

pcd = o3d.io.read_point_cloud("../../TestData/ sync_1.ply")

print(np.asarray(pcd.points))

One of the Point Cloud registration algorithm: http://www.open3d.org/docs/0.12.0/tutorial/pipelines/icp_registration.html

Problem statement 2: There are 15 point clouds provided. The task is to a). find overlapping and non overlapping point cloud pairs b). % overlap between those pairs.

import open3d as o3d

pcd = o3d.io.read_point_cloud("../c1_0_voxelpoints.ply")

print(np.asarray(pcd.points), np.asarray(pcd.colors))

Here pcd.points are 3d coordinates and pcd.colors (range is [0, 1], multiply * 255. to get below values) are rgb values/ segment output label.

label_to_rgb_mapping={
    'wall':[192,192,128],
    'floor':[128,0,0],
    'ceiling':[0,128,0],
    'windowpane':[128,128,0],
    'person':[0,0,128],
    'door':[128,0,128],
    'lamp':[128,128,128],
    'signboard':[64,0,0],
    'counter':[192,0,0],
    'storage':[64,128,0],
    'screen':[192,128,0],
    'beverage_machine':[64,0,128],
    'kitchen':[192,0,128],
    'products':[0,128,128],
    'pos_machine': [64,64,128],
    'others':[64,128,128],
    'rollergrill': [64,64,64]
    
}


