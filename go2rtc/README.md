go2rtc
=========

Ansible go2rtc role
https://github.com/AlexxIT/go2rtc


Role Variables
--------------
Default variable values:
```yaml
go2rtc_group: go2rtc
go2rtc_user: go2rtc
go2rtc_dir: /opt/go2rtc
go2rtc_settings_file: /opt/go2rtc/go2rtc.yaml
go2rtc_version: v1.6.2
go2rtc_arch: arm64

camera_id: 0
video_width: 1920
video_height: 1080

webrtc_port: 8555
api_listen_address: 127.0.0.1:1984
rtsp_listen_address: 127.0.0.1:8554

log_global_level: info
```


Example Playbook
----------------

```yaml
---
- name: use go2rtc role playbook
  hosts: vim3-pro
  user: khadas
  become: true

  roles:
    - role: go2rtc
      api_listen_address: "{{ ansible_host }}:1984"
      rtsp_listen_address: "{{ ansible_host }}:8554"
      camera_id: 1

```

License
-------

MIT

Author Information
------------------

Andrew Dorokhin 
