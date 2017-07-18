Ansible Role: Image Resize
=========

This role help resize an image to specific size. Basically, it uses ImageMagick package --size option.

Requirements
------------

yum

Role Variables
--------------

| Name                    | Default value                         |        Requird       | Description                                                                 |
|-------------------------|---------------------------------------|----------------------|-----------------------------------------------------------------------------|
| input_img               | sample-openshift-ori.png              |         no           | Original Image InputPath                                                    |
| output_img              | /tmp/sample-openshift-ori-resize.png  |         no           | Resized Image Output Path                                                   |
| size                    | 193x144                               |         no           | Resized Image Size                                                          |
| overwrite_force         | false                                 |         no           | Overwrite Exist Image                                                       |
| temp_dir	          | /tmp	                          |         no           | Temp directory


Dependencies
------------

None

Example Playbook
----------------
~~~
- name: Example Playbook
  hosts: localhost
  gather_facts: false

  roles:
   - { role: Jooho.image-resize }
   #- { role: Jooho.image-resize, input_img: "original-image.png", output_img: "resize-image.png", size: "193x44", overwrite_force: "true" }
~~~
License
-------

BSD/MIT

Author Information
------------------

This role was created in 2016 by [Jooho Lee](http://github.com/jooho).
