There are some issues with nextcloud when it's working behind proxy. 

To fix that, in addition to configuration provided in docker-compose I've added that values to config.php: 
  ```
  'trusted_proxies' => ['traefik'],
  'overwriteprotocol' => 'https',
  ```
  
  and changed `'overwrite.cli.url' => 'https://s.48n.in',`
  
  For the next version probably it will be possible to do that from environment variables: 
