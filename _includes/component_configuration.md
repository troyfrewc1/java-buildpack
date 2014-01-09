## Configuration

For general information on configuring the buildpack, refer to [Configuration and Extension][ce].

The component can be configured by modifying the [`config/{{page.component_id}}.yml`][cf] file.  The component uses the [`Repository` utility support][r] and so it supports the [version syntax][v] defined there.

| Name | Description
| ---- | -----------
| `repository_root` | The URL of the component repository index ([details][r]).
| `version` | The version of component to use. Candidate versions can be found in [this listing][l].

[ce]: ../index.html#Configuration-and-Extension
[cf]: https://github.com/cloudfoundry/java-buildpack/blob/master/config/{{page.component_id}}.yml
[l]: http://download.pivotal.io.s3.amazonaws.com/{{page.repo_root}}/index.yml
[r]: extending/repositories.html
[v]: extending/repositories.html#version-syntax-and-ordering
