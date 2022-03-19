# lighttpd Configuration for GetSimple CMS


$HTTP["host"] =~ "domain_for_GetSimple" {
        server.document-root = "/var/www/path_for_GetSimple"
        index-file.names = ( "index.php" )
        url.access-deny = ( ".xml" )
        url.rewrite = ( "/(admin)/?(.*)" => "$0", "/([A-Za-z0-9_-]+)/?$" => "/?id=$1" )
}
