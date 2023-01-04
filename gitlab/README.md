#GitLab - Docker Compose

<pre>
mkdir gitlab
export GITLAB_HOME=$(pwd)/gitlab

[root@c7 gitlab]# docker-compose up -d
Creating network "gitlab-network" with the default driver
Pulling web (gitlab/gitlab-ce:latest)...
latest: Pulling from gitlab/gitlab-ce
846c0b181fff: Pull complete
4e9f37801cd6: Pull complete
433d95578d03: Pull complete
d0506f369eef: Pull complete
4b8b41985700: Pull complete
f303beab1337: Pull complete
421107247076: Pull complete
97ebf54f2cd8: Pull complete
Pulling gitlab-runner (gitlab/gitlab-runner:alpine)...
alpine: Pulling from gitlab/gitlab-runner
9621f1afde84: Pull complete
fc777c8f525f: Pull complete
64596e3b14f8: Pull complete
Creating gitlab-ce ... done
Creating gitlab-runner ... done
[root@c7 gitlab]# docker-compose ps -a
List containers.

Usage: ps [options] [SERVICE...]

Options:
    -q, --quiet          Only display IDs
    --services           Display services
    --filter KEY=VAL     Filter services by a property
[root@c7 gitlab]# docker-compose ps
    Name                   Command                  State                                             Ports
--------------------------------------------------------------------------------------------------------------------------------------------------
gitlab-ce       /assets/wrapper                  Up (healthy)   22/tcp, 0.0.0.0:8443->443/tcp,:::8443->443/tcp,
                                                                0.0.0.0:8080->80/tcp,:::8080->80/tcp
gitlab-runner   /usr/bin/dumb-init /entryp ...   Up
[root@c7 gitlab]# docker exec -it gitlab-ce grep 'Password:' /etc/gitlab/initial_root_password
Password: HCvAFcTBNurQOxdP5L81ZnT5KYuuvh27BD8GYNUYlsw=
[root@c7 gitlab]#

</pre>
