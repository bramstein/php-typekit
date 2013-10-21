## Typekit PHP API Client

This is a PHP library that implements the [Typekit developers API](https://typekit.com/docs/api). It allows you to create, retrieve, delete, update, and publish Typekit kits from your PHP code.

## API

To use the Typekit client, include `typekit-client.php` in your page and create a new instance of the client.

    $typekit = new Typekit();

The following methods are available:

 * `create(data, token)` Create a new kit;
 * `remove(kit_id, token)` Remove an existing kit;
 * `update(kit_id, data, token)` Update an existing kit;
 * `publish(kit_id, token)` Publish an existing kit;
 * `get(kit_id)` Get a published kit;
 * `get(kit_id, token)` Get an unpublished kit;
 * `get(null, token)` Return all kits.

For example, to create a new kit you call the `create` method with the kit data and your Typekit API token:

    $kit = $typekit->create([
        "name" => "Example",
        "families" => [[ "id" => "gkmg" ]]
        "domains" => ["*.example.com"]
    ], 'xxxxx');


## Copyright and License

Typekit PHP API Client (c) 2013 Adobe Systems Incorporated.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License.  You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
