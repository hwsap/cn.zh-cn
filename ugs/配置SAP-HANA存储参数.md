# 配置SAP HANA存储参数<a name="saphana_02_0039"></a>

配置SAP HANA存储的参数，满足SAP公司的要求。

SAP HANA 1.0才需要进行配置，因SAP HANA 2.0中默认的配置已经符合要求，不需要配置。

更多信息，可参见以下内容：

-   SAP Note 2186744 - FAQ: SAP HANA Parameters
-   SAP Note 2267798 - Configuration of the SAP HANA Database during Installation Using hdbparam
-   [SAP\_HANA\_Administration\_Guide](https://help.sap.com/viewer/6b94445c94ae495c83a19646e7c3fd56/2.0.01/en-US)
-   SAP Note 2156526 - Parameter constraint validation on section indicies does not work correctly with hdbparam
-   SAP Note 2399079 - Elimination of hdbparam in HANA 2

## 操作步骤<a name="section3133031319426"></a>

1.  登录SAP HANA节点。
2.  切换到SAP HANA管理员模式。

    **su -  _s00_adm**

3.  配置存储参数。

    **hdbparam --paramset fileio.async\_read\_submit=on**

    **hdbparam --paramset fileio.async\_write\_submit\_active=on**

    **hdbparam --paramset fileio.async\_write\_submit\_blocks=all**

4.  （可选）参考上述步骤，在其他SAP HANA节点上配置。

    存在多个SAP HANA节点时，需要在其他SAP HANA节点上进行同样的配置。


