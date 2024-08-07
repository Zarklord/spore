# Spore LuaAPI
<web-summary>Extends the Spore ModAPI to add support for Lua mods</web-summary>
<link-summary>Write spore mods in Lua</link-summary>
<card-summary>Write spore mods in Lua</card-summary>

<include from="Snippets.topic" element-id="requires-mod-api"/>
<include from="Snippets.topic" element-id="api-only-mod"/>
<include from="Snippets.topic" element-id="beta-mod"/>

This Mod Uses the Mod API to allow you to write mods for spore in Lua.

<include from="Snippets.topic" element-id="mod-download-experimental">
    <var name="download" value="https://github.com/Zarklord/Spore-LuaAPI/releases/download/v1.0.0-prerelease-1/Spore-LuaAPIv1.0.0-prerelease-1.sporemod"/>
    <var name="issue" value="https://github.com/Zarklord/Spore-LuaAPI/issues"/>
</include>

## Version History
<deflist collapsible="true" default-state="collapsed">
    <def title="v1.0.0 prerelease 1" default-state="expanded">
        <list>
            <li>Mods now use modimport/ModImportOnAllThreads instead of require/RequireOnAllThreads.</li>
            <li>Fixed a crash from LuaMultiReference returning temporaries.</li>
            <li>All bindings now have proper tostring and == metamethods set.</li>
            <li>InitializePropManager and LuaConsole won't crash the game when the game is shutting down.</li>
            <li>ExecuteOnAllThreads now properly copies upvalues, and has the default error handler.</li>
        </list>
    </def>
    <def title="v1.0.0 beta 2">
        <list>
            <li>Added a proper callstack logging when a lua crash occurs.</li>
            <li>Added tostring metamethods to most basic property types.</li>
            <li>Fixed a bug when setting property's of type bool, int32, uint32, or float.</li>
        </list>
    </def>
    <def title="v1.0.0 beta 1">
        <list>
            <li>Lua mod's can be embedded into packages.</li>
            <li>Functions in the global environment can be called directly via the cheat console (the cheat console has been modified to be capable of running Lua code).</li>
            <li>Currently, the following Spore ModAPI types have been exposed to lua:
                <list>
                    <li>Resource::IKeyFilter</li>
                    <li>App::Property</li>
                    <li>App::PropertyList</li>
                    <li>App::IPropManager</li>
                    <li>ResourceKey</li>
                    <li>TextProperty</li>
                    <li>LocalizedString</li>
                    <li>Vector2</li>
                    <li>Vector3</li>
                    <li>Vector4</li>
                    <li>ColorRGB</li>
                    <li>ColorRGBA</li>
                    <li>Matrix</li>
                    <li>Transform</li>
                    <li>BoundingBox</li>
                </list>
            </li>
            <li>The tracy profiler has been implemented as well, you can download the profiler application from here to connect to a running spore game.</li>
        </list>
    </def>
</deflist>

<seealso style="cards">
    <category ref="external">
        <a href="https://github.com/Zarklord/Spore-LuaAPI/" summary="Source Code">Github</a>
    </category>
    <category ref="docs">
        <a href="https://zarklord.github.io/Spore-LuaAPI/documentation.html" summary="Spore LuaAPI Docs">Modding Documentation</a>
    </category>
</seealso>