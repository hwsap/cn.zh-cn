# Scale Up和Scale Out<a name="saphana_02_0005"></a>

从节点扩展方式区分：SAP HANA可以分为Scale Up和Scale Out两种架构。

-   Scale Up：称为单节点系统，指系统中只包括一个有效节点（如果需要HA时，可以将两个单节点以System Replication形式构成单节点的HA架构）。这种架构的系统只具有垂直扩展能力，当需要扩展系统时，通过在节点上增加更多的CPU、内存和硬盘来扩大系统的能力。

    目前暂不支持SAP HANA运行时，对该节点在线扩大能力，例如增加更多的CPU、内存或硬盘。

-   Scale Out：称为集群系统。指由多个节点组成的SAP HANA系统，这种系统的扩展主要以水平扩展方式（指增加节点的方式）来进行。

