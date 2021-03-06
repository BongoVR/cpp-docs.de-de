# [OLE DB-Programmierung](ole-db-programming.md)
## [Übersicht über die OLE DB-Programmierung](ole-db-programming-overview.md)
### [OLE DB-Consumer und -Anbieter](ole-db-consumers-and-providers.md)
### [OLE DB-Objektmodell](ole-db-object-model.md)
### [Vorlagen, Attribute und andere Implementierungen von OLE DB](ole-db-templates-attributes-and-other-implementations.md)
### [Fragen zum OLE DB-Architekturdesign](ole-db-architectural-design-issues.md)
## [OLE DB-Consumervorlagen (C++)](ole-db-consumer-templates-cpp.md)
### [Datenquellen und Sitzungen](data-sources-and-sessions.md)
### [Accessoren und Rowsets](accessors-and-rowsets.md)
### [Befehle und Tabellen](commands-and-tables.md)
### [Benutzerdatensätze](user-records.md)
### [Schemarowsets](schema-rowsets.md)
### [Erstellen eines OLE DB-Consumers](creating-an-ole-db-consumer.md)
#### [Erstellen eines OLE DB-Consumers mit einem Assistenten](creating-an-ole-db-consumer-using-a-wizard.md)
##### [Erstellen eines einfachen Consumers](creating-a-simple-consumer.md)
##### [Implementieren eines einfachen Consumers](implementing-a-simple-consumer.md)
##### [Vom Consumer-Assistenten generierte Klassen](consumer-wizard-generated-classes.md)
##### [Vom Consumer-Assistenten generierte Methoden](consumer-wizard-generated-methods.md)
#### [Erstellen eines Consumers ohne Assistent](creating-a-consumer-without-using-a-wizard.md)
### [Arbeiten mit OLE DB-Consumervorlagen](working-with-ole-db-consumer-templates.md)
#### [Vereinfachen des Datenzugriffs mit Datenbankattributen](simplifying-data-access-with-database-attributes.md)
#### [Feldstatus-Datenmember in vom Assistenten generierten Zugriffsmethoden](field-status-data-members-in-wizard-generated-accessors.md)
#### [Durchlaufen eines einfachen Rowsets](traversing-a-simple-rowset.md)
#### [Ausgeben einer parametrisierten Abfrage](issuing-a-parameterized-query.md)
#### [Abrufen von Daten](fetching-data.md)
#### [Aktualisieren von Rowsets](updating-rowsets.md)
#### [Verwenden von gespeicherten Prozeduren](using-stored-procedures.md)
##### [Definieren von gespeicherten Prozeduren](defining-stored-procedures.md)
##### [Ausgabeparameter](output-parameters.md)
##### [Verwenden mehrerer Resultsets aus einer gespeicherten Prozedur](using-multiple-result-sets-from-one-stored-procedure.md)
#### [Verwenden von Zugriffsmethoden](using-accessors.md)
##### [Bestimmen des geeigneten Zugriffsmethodentyps](determining-which-type-of-accessor-to-use.md)
##### [Verwenden mehrerer Zugriffsmethoden für ein Rowset](using-multiple-accessors-on-a-rowset.md)
##### [Verwenden von dynamischen Zugriffsmethoden](using-dynamic-accessors.md)
##### [Überschreiben einer dynamischen Zugriffsmethode](overriding-a-dynamic-accessor.md)
##### [Verwenden von manuellen Zugriffsmethoden](using-manual-accessors.md)
##### [Zugreifen auf XML-Daten](accessing-xml-data.md)
#### [Abrufen von Metadaten mit Schemarowsets](obtaining-metadata-with-schema-rowsets.md)
#### [Unterstützen von Transaktionen in OLE DB](supporting-transactions-in-ole-db.md)
#### [Verwenden von OLE DB-Datensatzansichten](using-ole-db-record-views.md)
#### [Verwenden eines vorhandenen ADO-Recordsets](using-an-existing-ado-recordset.md)
#### [Aktualisieren einer Spalte, wenn eine andere Tabelle einen Verweis auf die Zeile enthält](updating-a-column-when-another-table-contains-a-reference-to-the-row.md)
#### [Verwenden von Lesezeichen](using-bookmarks.md)
#### [Abrufen eines BLOBs](retrieving-a-blob.md)
#### [Empfangen von Benachrichtigungen](receiving-notifications.md)
## [OLE DB-Anbietervorlagen (C++)](ole-db-provider-templates-cpp.md)
### [Architektur von OLE DB-Anbietervorlagen](ole-db-provider-template-architecture.md)
#### [Datenquellenobjekt-Schnittstellen](data-source-object-interfaces.md)
#### [Sitzungsobjekt-Schnittstellen](session-object-interfaces.md)
#### [Rowsetobjekt-Schnittstellen](rowset-object-interfaces.md)
#### [Befehlsobjekt-Schnittstellen](command-object-interfaces.md)
#### [Transaktionsobjekt-Schnittstellen](transaction-object-interfaces.md)
#### [Eigenschaftenzuordnungen](property-maps.md)
#### [Benutzerdatensatz](user-record.md)
### [Erstellen eines OLE DB-Anbieters](creating-an-ole-db-provider.md)
#### [Erstellen eines Projekts für den Anbieter](creating-a-project-for-the-provider.md)
#### [Erstellen des Anbieters](creating-the-provider.md)
#### [Vom Anbieter-Assistenten generierte Dateien](provider-wizard-generated-files.md)
##### [CMyProviderSource (MyProviderDS.H)](cmyprovidersource-myproviderds-h.md)
##### [CMyProviderSession (MyProviderSess.H)](cmyprovidersession-myprovidersess-h.md)
##### [CMyProviderCommand (MyProviderRS.H)](cmyprovidercommand-myproviderrs-h.md)
##### [CMyProviderRowset (MyProviderRS.H)](cmyproviderrowset-myproviderrs-h.md)
##### [CMyProviderWindowsFile](cmyproviderwindowsfile.md)
#### [Erstellen eines einfachen schreibgeschützten Anbieters](creating-a-simple-read-only-provider.md)
##### [Implementieren des einfachen schreibgeschützten Anbieters](implementing-the-simple-read-only-provider.md)
###### [Einlesen von Zeichenfolgen in den OLE DB-Anbieter](reading-strings-into-the-ole-db-provider.md)
###### [Speichern von Zeichenfolgen im OLE DB-Anbieter](storing-strings-in-the-ole-db-provider.md)
##### [Erweitern des einfachen schreibgeschützten Anbieters](enhancing-the-simple-read-only-provider.md)
###### [Ändern der Vererbung von "RMyProviderRowset"](modifying-the-inheritance-of-rmyproviderrowset.md)
###### [Dynamisches Festlegen der an den Consumer zurückgegebenen Spalten](dynamically-determining-columns-returned-to-the-consumer.md)
##### [Testen des schreibgeschützten Anbieters](testing-the-read-only-provider.md)
#### [Erstellen eines aktualisierbaren Anbieters](creating-an-updatable-provider.md)
### [Arbeiten mit OLE DB-Anbietervorlagen](working-with-ole-db-provider-templates.md)
#### [Hinzufügen einer Schnittstelle zum Anbieter](adding-an-interface-to-your-provider.md)
#### [Verweisen auf eine Eigenschaft im Anbieter](referencing-a-property-in-your-provider.md)
#### [Festlegen von Eigenschaften im Anbieter](setting-properties-in-your-provider.md)
#### [Dynamisches Binden von Spalten im Anbieter](dynamically-binding-columns-in-your-provider.md)
#### [Unterstützen des Freethreadings im Anbieter](supporting-free-threading-in-your-provider.md)
#### [Testen des Anbieters](testing-your-provider.md)
#### [Debuggen des Anbieters](debugging-your-provider.md)
#### [Konvertieren von Daten, die nicht vom Anbieter unterstützt werden](converting-data-not-supported-by-the-provider.md)
### [Erweiterte Anbietertechniken](advanced-provider-techniques.md)
#### [Unterstützen von Benachrichtigungen](supporting-notifications.md)
#### [Supporting Schema Rowsets](supporting-schema-rowsets.md)
#### [Anbieterunterstützung für Lesezeichen](provider-support-for-bookmarks.md)
#### [Erfolgreiche Durchführung der OLE DB-Konformitätstests](passing-ole-db-conformance-tests.md)
#### [OLE DB-Ressourcenpooling und -Dienste](ole-db-resource-pooling-and-services.md)
##### [Ressourcenpooling in OLE DB-Anwendungen](resource-pooling-in-your-ole-db-application.md)
##### [Aktivieren und Deaktivieren von OLE DB-Diensten](enabling-and-disabling-ole-db-services.md)
###### [Aktivieren und Deaktivieren von Diensten für einen Anbieter](enabling-and-disabling-services-for-a-provider.md)
###### [Überschreiben der Standardwerte für Anbieterdienste](overriding-provider-service-defaults.md)
# [OLE DB-Vorlagen](ole-db-templates.md)
## [Referenz der OLE DB-Consumervorlagen](ole-db-consumer-templates-reference.md)
### [CAccessor-Klasse](caccessor-class.md)
### [CAccessorBase-Klasse](caccessorbase-class.md)
#### [CAccessorBase::Close](caccessorbase-close.md)
#### [CAccessorBase::GetHAccessor](caccessorbase-gethaccessor.md)
#### [CAccessorBase::GetNumAccessors](caccessorbase-getnumaccessors.md)
#### [CAccessorBase::IsAutoAccessor](caccessorbase-isautoaccessor.md)
#### [CAccessorBase::ReleaseAccessors](caccessorbase-releaseaccessors.md)
### [CAccessorRowset-Klasse](caccessorrowset-class.md)
#### [CAccessorRowset-Members](caccessorrowset-members.md)
#### [CAccessorRowset-Methoden](caccessorrowset-methods.md)
#### [CAccessorRowset::Bind](caccessorrowset-bind.md)
#### [CAccessorRowset::CAccessorRowset](caccessorrowset-caccessorrowset.md)
#### [CAccessorRowset::Close](caccessorrowset-close.md)
#### [CAccessorRowset::FreeRecordMemory](caccessorrowset-freerecordmemory.md)
#### [CAccessorRowset::GetColumnInfo](caccessorrowset-getcolumninfo.md)
### [CArrayRowset-Klasse](carrayrowset-class.md)
#### [CArrayRowset::CArrayRowset](carrayrowset-carrayrowset.md)
#### [CArrayRowset::m_nRowsRead](carrayrowset-m-nrowsread.md)
#### [CArrayRowset::operator](carrayrowset-operator.md)
#### [CArrayRowset::Snapshot](carrayrowset-snapshot.md)
### [CBookmark-Klasse](cbookmark-class.md)
#### [CBookmark::CBookmark](cbookmark-cbookmark.md)
#### [CBookmark::GetBuffer](cbookmark-getbuffer.md)
#### [CBookmark::GetSize](cbookmark-getsize.md)
#### [CBookmark::operator =](cbookmark-operator-equal.md)
#### [CBookmark::SetBookmark](cbookmark-setbookmark.md)
### [CBulkRowset-Klasse](cbulkrowset-class.md)
#### [CBulkRowset::AddRefRows](cbulkrowset-addrefrows.md)
#### [CBulkRowset::CBulkRowset](cbulkrowset-cbulkrowset.md)
#### [CBulkRowset::MoveFirst](cbulkrowset-movefirst.md)
#### [CBulkRowset::MoveLast](cbulkrowset-movelast.md)
#### [CBulkRowset::MoveNext](cbulkrowset-movenext.md)
#### [CBulkRowset::MovePrev](cbulkrowset-moveprev.md)
#### [CBulkRowset::MoveToBookmark](cbulkrowset-movetobookmark.md)
#### [CBulkRowset::MoveToRatio](cbulkrowset-movetoratio.md)
#### [CBulkRowset::ReleaseRows](cbulkrowset-releaserows.md)
#### [CBulkRowset::SetRows](cbulkrowset-setrows.md)
### [CColumnAccessor-Klasse](ccolumnaccessor-class.md)
### [CCommand-Klasse](ccommand-class.md)
#### [CCommand::Close](ccommand-close.md)
#### [CCommand::Create](ccommand-create.md)
#### [CCommand::CreateCommand](ccommand-createcommand.md)
#### [CCommand::GetNextResult](ccommand-getnextresult.md)
#### [CCommand::GetParameterInfo](ccommand-getparameterinfo.md)
#### [CCommand::Open](ccommand-open.md)
#### [CCommand::Prepare](ccommand-prepare.md)
#### [CCommand::ReleaseCommand](ccommand-releasecommand.md)
#### [CCommand::SetParameterInfo](ccommand-setparameterinfo.md)
#### [CCommand::Unprepare](ccommand-unprepare.md)
### [CDataConnection-Klasse](cdataconnection-class.md)
#### [CDataConnection::CDataConnection](cdataconnection-cdataconnection.md)
#### [CDataConnection::Copy](cdataconnection-copy.md)
#### [CDataConnection::Open](cdataconnection-open.md)
#### [CDataConnection::OpenNewSession](cdataconnection-opennewsession.md)
#### [CDataConnection::operator bool](cdataconnection-operator-bool.md)
#### [CDataConnection::operator bool (OLE DB)](cdataconnection-operator-bool-ole-db.md)
#### [CDataConnection::operator CDataSource&](cdataconnection-operator-cdatasource-amp.md)
#### [CDataConnection::operator CDataSource*](cdataconnection-operator-cdatasource-star.md)
#### [CDataConnection::operator CSession&](cdataconnection-operator-csession-amp.md)
#### [CDataConnection::operator CSession*](cdataconnection-operator-csession-star.md)
### [CDataSource-Klasse](cdatasource-class.md)
#### [DataSource::Close](cdatasource-close.md)
#### [DataSource::GetInitializationString](cdatasource-getinitializationstring.md)
#### [CDataSource::GetProperties](cdatasource-getproperties.md)
#### [DataSource::GetProperty](cdatasource-getproperty.md)
#### [CDataSource::Open](cdatasource-open.md)
#### [CDataSource::OpenFromFileName](cdatasource-openfromfilename.md)
#### [CDataSource::OpenFromInitializationString](cdatasource-openfrominitializationstring.md)
#### [CDataSource::OpenWithPromptFileName](cdatasource-openwithpromptfilename.md)
#### [CDataSource::OpenWithServiceComponents](cdatasource-openwithservicecomponents.md)
### [CDBErrorInfo-Klasse](cdberrorinfo-class.md)
#### [CDBErrorInfo::GetAllErrorInfo](cdberrorinfo-getallerrorinfo.md)
#### [CDBErrorInfo::GetBasicErrorInfo](cdberrorinfo-getbasicerrorinfo.md)
#### [CDBErrorInfo::GetCustomErrorObject](cdberrorinfo-getcustomerrorobject.md)
#### [CDBErrorInfo::GetErrorInfo](cdberrorinfo-geterrorinfo.md)
#### [CDBErrorInfo::GetErrorParameters](cdberrorinfo-geterrorparameters.md)
#### [CDBErrorInfo::GetErrorRecords](cdberrorinfo-geterrorrecords.md)
### [CDBPropIDSet-Klasse](cdbpropidset-class.md)
#### [CDBPropIDSet::AddPropertyID](cdbpropidset-addpropertyid.md)
#### [CDBPropIDSet::CDBPropIDSet](cdbpropidset-cdbpropidset.md)
#### [CDBPropIDSet::operator =](cdbpropidset-operator-equal.md)
#### [CDBPropIDSet::SetGUID](cdbpropidset-setguid.md)
### [CDBPropSet-Klasse](cdbpropset-class.md)
#### [CDBPropSet::AddProperty](cdbpropset-addproperty.md)
#### [CDBPropSet::CDBPropSet](cdbpropset-cdbpropset.md)
#### [CDBPropSet::operator =](cdbpropset-operator-equal.md)
#### [CDBPropSet::SetGUID](cdbpropset-setguid.md)
### [CDynamicAccessor-Klasse](cdynamicaccessor-class.md)
#### [CDynamicAccessor::AddBindEntry](cdynamicaccessor-addbindentry.md)
#### [CDynamicAccessor::CDynamicAccessor](cdynamicaccessor-cdynamicaccessor.md)
#### [CDynamicAccessor::Close](cdynamicaccessor-close.md)
#### [CDynamicAccessor::GetBlobHandling](cdynamicaccessor-getblobhandling.md)
#### [CDynamicAccessor::GetBlobSizeLimit](cdynamicaccessor-getblobsizelimit.md)
#### [CDynamicAccessor::GetBookmark](cdynamicaccessor-getbookmark.md)
#### [CDynamicAccessor::GetColumnCount](cdynamicaccessor-getcolumncount.md)
#### [CDynamicAccessor::GetColumnFlags](cdynamicaccessor-getcolumnflags.md)
#### [CDynamicAccessor::GetColumnInfo](cdynamicaccessor-getcolumninfo.md)
#### [CDynamicAccessor::GetColumnName](cdynamicaccessor-getcolumnname.md)
#### [CDynamicAccessor::GetColumnType](cdynamicaccessor-getcolumntype.md)
#### [CDynamicAccessor::GetLength](cdynamicaccessor-getlength.md)
#### [CDynamicAccessor::GetOrdinal](cdynamicaccessor-getordinal.md)
#### [CDynamicAccessor::GetStatus](cdynamicaccessor-getstatus.md)
#### [CDynamicAccessor::GetValue](cdynamicaccessor-getvalue.md)
#### [CDynamicAccessor::SetBlobHandling](cdynamicaccessor-setblobhandling.md)
#### [CDynamicAccessor::SetBlobSizeLimit](cdynamicaccessor-setblobsizelimit.md)
#### [CDynamicAccessor::SetLength](cdynamicaccessor-setlength.md)
#### [CDynamicAccessor::SetStatus](cdynamicaccessor-setstatus.md)
#### [CDynamicAccessor::SetValue](cdynamicaccessor-setvalue.md)
### [CDynamicParameterAccessor-Klasse](cdynamicparameteraccessor-class.md)
#### [CDynamicParameterAccessor::CDynamicParameterAccessor](cdynamicparameteraccessor-cdynamicparameteraccessor.md)
#### [CDynamicParameterAccessor::GetParam](cdynamicparameteraccessor-getparam.md)
#### [CDynamicParameterAccessor::GetParamCount](cdynamicparameteraccessor-getparamcount.md)
#### [CDynamicParameterAccessor::GetParamIO](cdynamicparameteraccessor-getparamio.md)
#### [CDynamicParameterAccessor::GetParamLength](cdynamicparameteraccessor-getparamlength.md)
#### [CDynamicParameterAccessor::GetParamName](cdynamicparameteraccessor-getparamname.md)
#### [CDynamicParameterAccessor::GetParamStatus](cdynamicparameteraccessor-getparamstatus.md)
#### [CDynamicParameterAccessor::GetParamString](cdynamicparameteraccessor-getparamstring.md)
#### [CDynamicParameterAccessor::GetParamType](cdynamicparameteraccessor-getparamtype.md)
#### [CDynamicParameterAccessor::SetParam](cdynamicparameteraccessor-setparam.md)
#### [CDynamicParameterAccessor::SetParamLength](cdynamicparameteraccessor-setparamlength.md)
#### [CDynamicParameterAccessor::SetParamStatus](cdynamicparameteraccessor-setparamstatus.md)
#### [CDynamicParameterAccessor::SetParamString](cdynamicparameteraccessor-setparamstring.md)
### [CDynamicStringAccessor-Klasse](cdynamicstringaccessor-class.md)
#### [CDynamicStringAccessor::GetString](cdynamicstringaccessor-getstring.md)
#### [CDynamicStringAccessor::SetString](cdynamicstringaccessor-setstring.md)
### [CDynamicStringAccessorA-Klasse](cdynamicstringaccessora-class.md)
### [CDynamicStringAccessorW-Klasse](cdynamicstringaccessorw-class.md)
### [CEnumerator-Klasse](cenumerator-class.md)
#### [CEnumerator::Find](cenumerator-find.md)
#### [CEnumerator::GetMoniker](cenumerator-getmoniker.md)
#### [CEnumerator::Open](cenumerator-open.md)
### [CEnumeratorAccessor-Klasse](cenumeratoraccessor-class.md)
#### [CEnumeratorAccessor::m_bIsParent](cenumeratoraccessor-m-bisparent.md)
#### [CEnumeratorAccessor::m_nType](cenumeratoraccessor-m-ntype.md)
#### [CEnumeratorAccessor::m_szDescription](cenumeratoraccessor-m-szdescription.md)
#### [CEnumeratorAccessor::m_szName](cenumeratoraccessor-m-szname.md)
#### [CEnumeratorAccessor::m_szParseName](cenumeratoraccessor-m-szparsename.md)
### [CManualAccessor-Klasse](cmanualaccessor-class.md)
#### [CManualAccessor::AddBindEntry](cmanualaccessor-addbindentry.md)
#### [CManualAccessor::AddParameterEntry](cmanualaccessor-addparameterentry.md)
#### [CManualAccessor::CreateAccessor](cmanualaccessor-createaccessor.md)
#### [CManualAccessor::CreateParameterAccessor](cmanualaccessor-createparameteraccessor.md)
### [CMultipleResults-Klasse](cmultipleresults-class.md)
### [CNoAccessor-Klasse](cnoaccessor-class.md)
### [CNoMultipleResults-Klasse](cnomultipleresults-class.md)
### [CNoRowset-Klasse](cnorowset-class.md)
### [CRestrictions-Klasse](crestrictions-class.md)
#### [CRestrictions::Open](crestrictions-open.md)
### [CRowset-Klasse](crowset-class.md)
#### [CRowset::AddRefRows](crowset-addrefrows.md)
#### [CRowset::Close](crowset-close.md)
#### [CRowset::Compare](crowset-compare.md)
#### [CRowset::CRowset](crowset-crowset.md)
#### [CRowset::Delete](crowset-delete.md)
#### [CRowset::FindNextRow](crowset-findnextrow.md)
#### [CRowset::GetApproximatePosition](crowset-getapproximateposition.md)
#### [CRowset::GetData](crowset-getdata.md)
#### [CRowset::GetDataHere](crowset-getdatahere.md)
#### [CRowset::GetOriginalData](crowset-getoriginaldata.md)
#### [CRowset::GetRowStatus](crowset-getrowstatus.md)
#### [CRowset::Insert](crowset-insert.md)
#### [CRowset::IsSameRow](crowset-issamerow.md)
#### [CRowset::MoveFirst](crowset-movefirst.md)
#### [CRowset::MoveLast](crowset-movelast.md)
#### [CRowset::MoveNext](crowset-movenext.md)
#### [CRowset::MovePrev](crowset-moveprev.md)
#### [CRowset::MoveToBookmark](crowset-movetobookmark.md)
#### [CRowset::MoveToRatio](crowset-movetoratio.md)
#### [CRowset::ReleaseRows](crowset-releaserows.md)
#### [CRowset::SetData](crowset-setdata.md)
#### [CRowset::Undo](crowset-undo.md)
#### [CRowset::Update](crowset-update.md)
#### [CRowset::UpdateAll](crowset-updateall.md)
### [CSession-Klasse](csession-class.md)
#### [CSession::Abort](csession-abort.md)
#### [CSession::Close](csession-close.md)
#### [CSession::Commit](csession-commit.md)
#### [CSession::GetTransactionInfo](csession-gettransactioninfo.md)
#### [CSession::Open](csession-open.md)
#### [CSession::StartTransaction](csession-starttransaction.md)
### [CStreamRowset-Klasse](cstreamrowset-class.md)
#### [CStreamRowset::Close](cstreamrowset-close.md)
#### [CStreamRowset::CStreamRowset](cstreamrowset-cstreamrowset.md)
### [CTable-Klasse](ctable-class.md)
#### [CTable::Open](ctable-open.md)
### [CXMLAccessor-Klasse](cxmlaccessor-class.md)
#### [CXMLAccessor::GetXMLColumnData](cxmlaccessor-getxmlcolumndata.md)
#### [CXMLAccessor::GetXMLRowData](cxmlaccessor-getxmlrowdata.md)
### [IRowsetNotifyImpl-Klasse](irowsetnotifyimpl-class.md)
#### [IRowsetNotifyImpl::OnFieldChange](irowsetnotifyimpl-onfieldchange.md)
#### [IRowsetNotifyImpl::OnRowChange](irowsetnotifyimpl-onrowchange.md)
#### [IRowsetNotifyImpl::OnRowsetChange](irowsetnotifyimpl-onrowsetchange.md)
### [Schemarowset-Klassen und Typedef-Klassen](schema-rowset-classes-and-typedef-classes.md)
#### [CAssertions, CAssertionInfo](cassertions-cassertioninfo.md)
#### [CCatalogs, CCatalogInfo](ccatalogs-ccataloginfo.md)
#### [CCharacterSets, CCharacterSetInfo](ccharactersets-ccharactersetinfo.md)
#### [CCheckConstraints, CCheckConstraintInfo](ccheckconstraints-ccheckconstraintinfo.md)
#### [CCollations, CCollationInfo](ccollations-ccollationinfo.md)
#### [CColumnDomainUsage, CColumnDomainUsageInfo](ccolumndomainusage-ccolumndomainusageinfo.md)
#### [CColumnPrivileges, CColumnPrivilegeInfo](ccolumnprivileges-ccolumnprivilegeinfo.md)
#### [CColumns, CColumnsInfo](ccolumns-ccolumnsinfo.md)
#### [CConstraintColumnUsage, CConstraintColumnUsageInfo](cconstraintcolumnusage-cconstraintcolumnusageinfo.md)
#### [CConstraintTableUsage, CConstraintTableUsageInfo](cconstrainttableusage-cconstrainttableusageinfo.md)
#### [CForeignKeys, CForeignKeysInfo](cforeignkeys-cforeignkeysinfo.md)
#### [CIndexes, CIndexInfo](cindexes-cindexinfo.md)
#### [KeyColumns, CKeyColumnInfo](ckeycolumns-ckeycolumninfo.md)
#### [CPrimaryKeys, CPrimaryKeyInfo](cprimarykeys-cprimarykeyinfo.md)
#### [CProcedureColumns, CProcedureColumnInfo](cprocedurecolumns-cprocedurecolumninfo.md)
#### [CProcedureParameters CProcedureParamInfo](cprocedureparameters-cprocedureparaminfo.md)
#### [CProcedures, CProcedureInfo](cprocedures-cprocedureinfo.md)
#### [CProviderTypes, CProviderInfo](cprovidertypes-cproviderinfo.md)
#### [CReferentialConstraints, CReferentialConstraintInfo](creferentialconstraints-creferentialconstraintinfo.md)
#### [CSchemata, CSchemataInfo](cschemata-cschematainfo.md)
#### [CSQLLanguages, CSQLLanguageInfo](csqllanguages-csqllanguageinfo.md)
#### [CStatistics, CStatisticInfo](cstatistics-cstatisticinfo.md)
#### [CTableConstraints, CTableConstraintInfo](ctableconstraints-ctableconstraintinfo.md)
#### [CTablePrivileges, CTablePrivilegeInfo](ctableprivileges-ctableprivilegeinfo.md)
#### [CTables, CTableInfo](ctables-ctableinfo.md)
#### [CTranslations, CTranslationInfo](ctranslations-ctranslationinfo.md)
#### [CUsagePrivileges, CUsagePrivilegeInfo](cusageprivileges-cusageprivilegeinfo.md)
#### [CViewColumnUsage, CViewColumnInfo](cviewcolumnusage-cviewcolumninfo.md)
#### [CViews, CViewInfo](cviews-cviewinfo.md)
#### [CViewTableUsage, CViewTableInfo](cviewtableusage-cviewtableinfo.md)
### [Makros und globale Funktionen für OLE-Consumervorlagen](macros-and-global-functions-for-ole-db-consumer-templates.md)
#### [AtlTraceErrorRecords](atltraceerrorrecords.md)
#### [BEGIN_ACCESSOR](begin-accessor.md)
#### [BEGIN_ACCESSOR_MAP](begin-accessor-map.md)
#### [BEGIN_COLUMN_MAP](begin-column-map.md)
#### [BEGIN_PARAM_MAP](begin-param-map.md)
#### [BLOB_ENTRY](blob-entry.md)
#### [BLOB_ENTRY_LENGTH](blob-entry-length.md)
#### [BLOB_ENTRY_LENGTH_STATUS](blob-entry-length-status.md)
#### [BLOB_ENTRY_STATUS](blob-entry-status.md)
#### [BLOB_NAME](blob-name.md)
#### [BLOB_NAME_LENGTH](blob-name-length.md)
#### [BLOB_NAME_LENGTH_STATUS](blob-name-length-status.md)
#### [BLOB_NAME_STATUS](blob-name-status.md)
#### [BOOKMARK_ENTRY](bookmark-entry.md)
#### [COLUMN_ENTRY](column-entry.md)
#### [COLUMN_ENTRY_EX](column-entry-ex.md)
#### [COLUMN_ENTRY_LENGTH](column-entry-length.md)
#### [COLUMN_ENTRY_LENGTH_STATUS](column-entry-length-status.md)
#### [COLUMN_ENTRY_PS](column-entry-ps.md)
#### [COLUMN_ENTRY_PS_LENGTH](column-entry-ps-length.md)
#### [COLUMN_ENTRY_PS_LENGTH_STATUS](column-entry-ps-length-status.md)
#### [COLUMN_ENTRY_PS_STATUS](column-entry-ps-status.md)
#### [COLUMN_ENTRY_STATUS](column-entry-status.md)
#### [COLUMN_ENTRY_TYPE](column-entry-type.md)
#### [COLUMN_ENTRY_TYPE_SIZE](column-entry-type-size.md)
#### [COLUMN_NAME](column-name.md)
#### [COLUMN_NAME_EX](column-name-ex.md)
#### [COLUMN_NAME_LENGTH](column-name-length.md)
#### [COLUMN_NAME_LENGTH_STATUS](column-name-length-status.md)
#### [COLUMN_NAME_PS](column-name-ps.md)
#### [COLUMN_NAME_PS_LENGTH](column-name-ps-length.md)
#### [COLUMN_NAME_PS_LENGTH_STATUS](column-name-ps-length-status.md)
#### [COLUMN_NAME_PS_STATUS](column-name-ps-status.md)
#### [COLUMN_NAME_STATUS](column-name-status.md)
#### [COLUMN_NAME_TYPE](column-name-type.md)
#### [COLUMN_NAME_TYPE_PS](column-name-type-ps.md)
#### [COLUMN_NAME_TYPE_SIZE](column-name-type-size.md)
#### [COLUMN_NAME_TYPE_STATUS](column-name-type-status.md)
#### [DEFINE_COMMAND](define-command.md)
#### [DEFINE_COMMAND_EX](define-command-ex.md)
#### [END_ACCESSOR](end-accessor.md)
#### [END_ACCESSOR_MAP](end-accessor-map.md)
#### [END_COLUMN_MAP](end-column-map.md)
#### [END_PARAM_MAP](end-param-map.md)
#### [SET_PARAM_TYPE](set-param-type.md)
## [Referenz der OLE DB-Anbietervorlagen](ole-db-provider-templates-reference.md)
### [CRowsetImpl-Klasse](crowsetimpl-class.md)
#### [CRowsetImpl::GetColumnInfo](crowsetimpl-getcolumninfo.md)
#### [CRowsetImpl::GetCommandFromID](crowsetimpl-getcommandfromid.md)
#### [CRowsetImpl::m_rgRowData](crowsetimpl-m-rgrowdata.md)
#### [CRowsetImpl::m_strCommandText](crowsetimpl-m-strcommandtext.md)
#### [CRowsetImpl::m_strIndexText](crowsetimpl-m-strindextext.md)
#### [CRowsetImpl::NameFromDBID](crowsetimpl-namefromdbid.md)
#### [CRowsetImpl::SetCommandText](crowsetimpl-setcommandtext.md)
#### [CRowsetImpl::ValidateCommandID](crowsetimpl-validatecommandid.md)
### [CSimpleRow-Klasse](csimplerow-class.md)
#### [CSimpleRow::AddRefRow](csimplerow-addrefrow.md)
#### [CSimpleRow::Compare](csimplerow-compare.md)
#### [CSimpleRow::CSimpleRow](csimplerow-csimplerow.md)
#### [CSimpleRow::m_dwRef](csimplerow-m-dwref.md)
#### [CSimpleRow::m_iRowset](csimplerow-m-irowset.md)
#### [CSimpleRow::ReleaseRow](csimplerow-releaserow.md)
### [CUtlProps-Klasse](cutlprops-class.md)
#### [CUtlProps::GetPropValue](cutlprops-getpropvalue.md)
#### [CUtlProps::IsValidValue](cutlprops-isvalidvalue.md)
#### [CUtlProps::OnInterfaceRequested](cutlprops-oninterfacerequested.md)
#### [CUtlProps::OnPropertyChanged](cutlprops-onpropertychanged.md)
#### [CUtlProps::SetPropValue](cutlprops-setpropvalue.md)
### [IAccessorImpl-Klasse](iaccessorimpl-class.md)
#### [IAccessorImpl::AddRefAccessor](iaccessorimpl-addrefaccessor.md)
#### [IAccessorImpl::CreateAccessor](iaccessorimpl-createaccessor.md)
#### [IAccessorImpl::GetBindings](iaccessorimpl-getbindings.md)
#### [IAccessorImpl::IAccessorImpl](iaccessorimpl-iaccessorimpl.md)
#### [IAccessorImpl::ReleaseAccessor](iaccessorimpl-releaseaccessor.md)
### [IColumnsInfoImpl-Klasse](icolumnsinfoimpl-class.md)
#### [IColumnsInfoImpl::GetColumnInfo](icolumnsinfoimpl-getcolumninfo.md)
#### [IColumnsInfoImpl::MapColumnIDs](icolumnsinfoimpl-mapcolumnids.md)
### [ICommandImpl-Klasse](icommandimpl-class.md)
#### [ICommandImpl::Cancel](icommandimpl-cancel.md)
#### [ICommandImpl::CancelExecution](icommandimpl-cancelexecution.md)
#### [ICommandImpl::CreateRowset](icommandimpl-createrowset.md)
#### [ICommandImpl::Execute](icommandimpl-execute.md)
#### [ICommandImpl::GetDBSession](icommandimpl-getdbsession.md)
#### [ICommandImpl::ICommandImpl](icommandimpl-icommandimpl.md)
#### [ICommandImpl::m_bCancel](icommandimpl-m-bcancel.md)
#### [ICommandImpl::m_bCancelWhenExecuting](icommandimpl-m-bcancelwhenexecuting.md)
#### [ICommandImpl::m_bIsExecuting](icommandimpl-m-bisexecuting.md)
### [ICommandPropertiesImpl-Klasse](icommandpropertiesimpl-class.md)
#### [ICommandPropertiesImpl::GetProperties](icommandpropertiesimpl-getproperties.md)
#### [ICommandPropertiesImpl::SetProperties](icommandpropertiesimpl-setproperties.md)
### [ICommandTextImpl-Klasse](icommandtextimpl-class.md)
#### [ICommandTextImpl::GetCommandText](icommandtextimpl-getcommandtext.md)
#### [ICommandTextImpl::m_strCommandText](icommandtextimpl-m-strcommandtext.md)
#### [ICommandTextImpl::SetCommandText](icommandtextimpl-setcommandtext.md)
### [IConvertTypeImpl-Klasse](iconverttypeimpl-class.md)
#### [IConvertTypeImpl::CanConvert](iconverttypeimpl-canconvert.md)
### [IDBCreateCommandImpl-Klasse](idbcreatecommandimpl-class.md)
#### [IDBCreateCommandImpl::CreateCommand](idbcreatecommandimpl-createcommand.md)
### [IDBCreateSessionImpl-Klasse](idbcreatesessionimpl-class.md)
#### [IDBCreateSessionImpl::CreateSession](idbcreatesessionimpl-createsession.md)
### [IDBInitializeImpl-Klasse](idbinitializeimpl-class.md)
#### [IDBInitializeImpl::IDBInitializeImpl](idbinitializeimpl-idbinitializeimpl.md)
#### [IDBInitializeImpl::Initialize](idbinitializeimpl-initialize.md)
#### [IDBInitializeImpl::m_dwStatus](idbinitializeimpl-m-dwstatus.md)
#### [IDBInitializeImpl::m_pCUtlPropInfo](idbinitializeimpl-m-pcutlpropinfo.md)
#### [IDBInitializeImpl::Uninitialize](idbinitializeimpl-uninitialize.md)
### [IDBPropertiesImpl-Klasse](idbpropertiesimpl-class.md)
#### [IDBPropertiesImpl::GetProperties](idbpropertiesimpl-getproperties.md)
#### [IDBPropertiesImpl::GetPropertyInfo](idbpropertiesimpl-getpropertyinfo.md)
#### [IDBPropertiesImpl::SetProperties](idbpropertiesimpl-setproperties.md)
### [IDBSchemaRowsetImpl-Klasse](idbschemarowsetimpl-class.md)
#### [IDBSchemaRowsetImpl::CheckRestrictions](idbschemarowsetimpl-checkrestrictions.md)
#### [IDBSchemaRowsetImpl::CreateSchemaRowset](idbschemarowsetimpl-createschemarowset.md)
#### [IDBSchemaRowsetImpl::GetRowset](idbschemarowsetimpl-getrowset.md)
#### [IDBSchemaRowsetImpl::GetSchemas](idbschemarowsetimpl-getschemas.md)
#### [IDBSchemaRowsetImpl::SetRestrictions](idbschemarowsetimpl-setrestrictions.md)
### [IErrorRecordsImpl-Klasse](ierrorrecordsimpl-class.md)
#### [IErrorRecordsImpl::AddErrorRecord](ierrorrecordsimpl-adderrorrecord.md)
#### [IErrorRecordsImpl::GetBasicErrorInfo](ierrorrecordsimpl-getbasicerrorinfo.md)
#### [IErrorRecordsImpl::GetCustomErrorObject](ierrorrecordsimpl-getcustomerrorobject.md)
#### [IErrorRecordsImpl::GetErrorDescriptionString](ierrorrecordsimpl-geterrordescriptionstring.md)
#### [IErrorRecordsImpl::GetErrorGUID](ierrorrecordsimpl-geterrorguid.md)
#### [IErrorRecordsImpl::GetErrorHelpContext](ierrorrecordsimpl-geterrorhelpcontext.md)
#### [IErrorRecordsImpl::GetErrorHelpFile](ierrorrecordsimpl-geterrorhelpfile.md)
#### [IErrorRecordsImpl::GetErrorInfo](ierrorrecordsimpl-geterrorinfo.md)
#### [IErrorRecordsImpl::GetErrorParameters](ierrorrecordsimpl-geterrorparameters.md)
#### [IErrorRecordsImpl::GetRecordCount](ierrorrecordsimpl-getrecordcount.md)
#### [IErrorRecordsImpl::GetErrorSource](ierrorrecordsimpl-geterrorsource.md)
#### [IErrorRecordsImpl::m_rgErrors](ierrorrecordsimpl-m-rgerrors.md)
### [IGetDataSourceImpl-Klasse](igetdatasourceimpl-class.md)
#### [IGetDataSourceImpl::GetDataSource](igetdatasourceimpl-getdatasource.md)
### [IOpenRowsetImpl-Klasse](iopenrowsetimpl-class.md)
#### [IOpenRowsetImpl::CreateRowset](iopenrowsetimpl-createrowset.md)
#### [IOpenRowsetImpl::OpenRowset](iopenrowsetimpl-openrowset.md)
### [IRowsetChangeImpl-Klasse](irowsetchangeimpl-class.md)
#### [IRowsetChangeImpl::DeleteRows](irowsetchangeimpl-deleterows.md)
#### [IRowsetChangeImpl::FlushData](irowsetchangeimpl-flushdata.md)
#### [IRowsetChangeImpl::InsertRow](irowsetchangeimpl-insertrow.md)
#### [IRowsetChangeImpl::SetData](irowsetchangeimpl-setdata.md)
### [IRowsetCreatorImpl-Klasse](irowsetcreatorimpl-class.md)
#### [IRowsetCreatorImpl::SetSite](irowsetcreatorimpl-setsite.md)
### [IRowsetIdentityImpl-Klasse](irowsetidentityimpl-class.md)
#### [IRowsetIdentityImpl::IsSameRow](irowsetidentityimpl-issamerow.md)
### [IRowsetImpl-Klasse](irowsetimpl-class.md)
#### [IRowsetImpl::AddRefRows](irowsetimpl-addrefrows.md)
#### [IRowsetImpl::CreateRow](irowsetimpl-createrow.md)
#### [IRowsetImpl::GetData](irowsetimpl-getdata.md)
#### [IRowsetImpl::GetDBStatus](irowsetimpl-getdbstatus.md)
#### [IRowsetImpl::GetNextRows](irowsetimpl-getnextrows.md)
#### [IRowsetImpl::IRowsetImpl](irowsetimpl-irowsetimpl.md)
#### [IRowsetImpl::m_bCanFetchBack](irowsetimpl-m-bcanfetchback.md)
#### [IRowsetImpl::m_bCanScrollBack](irowsetimpl-m-bcanscrollback.md)
#### [IRowsetImpl::m_bReset](irowsetimpl-m-breset.md)
#### [IRowsetImpl::m_iRowset](irowsetimpl-m-irowset.md)
#### [IRowsetImpl::m_rgRowHandles](irowsetimpl-m-rgrowhandles.md)
#### [IRowsetImpl::RefRows](irowsetimpl-refrows.md)
#### [IRowsetImpl::ReleaseRows](irowsetimpl-releaserows.md)
#### [IRowsetImpl::RestartPosition](irowsetimpl-restartposition.md)
#### [IRowsetImpl::SetDBStatus](irowsetimpl-setdbstatus.md)
### [IRowsetInfoImpl-Klasse](irowsetinfoimpl-class.md)
#### [IRowsetInfoImpl::GetProperties](irowsetinfoimpl-getproperties.md)
#### [IRowsetInfoImpl::GetReferencedRowset](irowsetinfoimpl-getreferencedrowset.md)
#### [IRowsetInfoImpl::GetSpecification](irowsetinfoimpl-getspecification.md)
### [IRowsetLocateImpl-Klasse](irowsetlocateimpl-class.md)
#### [IRowsetLocateImpl::Compare](irowsetlocateimpl-compare.md)
#### [IRowsetLocateImpl::GetRowsAt](irowsetlocateimpl-getrowsat.md)
#### [IRowsetLocateImpl::GetRowsByBookmark](irowsetlocateimpl-getrowsbybookmark.md)
#### [IRowsetLocateImpl::Hash](irowsetlocateimpl-hash.md)
#### [IRowsetLocateImpl::m_rgBookmarks](irowsetlocateimpl-m-rgbookmarks.md)
### [IRowsetNotifyCP-Klasse](irowsetnotifycp-class.md)
#### [IRowsetNotifyCP::Fire_OnFieldChange](irowsetnotifycp-fire-onfieldchange.md)
#### [IRowsetNotifyCP::Fire_OnRowChange](irowsetnotifycp-fire-onrowchange.md)
#### [IRowsetNotifyCP::Fire_OnRowsetChange](irowsetnotifycp-fire-onrowsetchange.md)
### [IRowsetUpdateImpl-Klasse](irowsetupdateimpl-class.md)
#### [IRowsetUpdateImpl::GetPendingRows](irowsetupdateimpl-getpendingrows.md)
#### [IRowsetUpdateImpl::GetOriginalData](irowsetupdateimpl-getoriginaldata.md)
#### [IRowsetUpdateImpl::GetRowStatus](irowsetupdateimpl-getrowstatus.md)
#### [IRowsetUpdateImpl::IsUpdateAllowed](irowsetupdateimpl-isupdateallowed.md)
#### [IRowsetUpdateImpl::m_mapCachedData](irowsetupdateimpl-m-mapcacheddata.md)
#### [IRowsetUpdateImpl::SetData](irowsetupdateimpl-setdata.md)
#### [IRowsetUpdateImpl::Undo](irowsetupdateimpl-undo.md)
#### [IRowsetUpdateImpl::Update](irowsetupdateimpl-update.md)
### [ISessionPropertiesImpl-Klasse](isessionpropertiesimpl-class.md)
#### [ISessionPropertiesImpl::GetProperties](isessionpropertiesimpl-getproperties.md)
#### [ISessionPropertiesImpl::SetProperties](isessionpropertiesimpl-setproperties.md)
### [Makros für OLE DB-Anbietervorlagen](macros-for-ole-db-provider-templates.md)
#### [BEGIN_PROPERTY_SET](begin-property-set.md)
#### [BEGIN_PROPERTY_SET_EX](begin-property-set-ex.md)
#### [BEGIN_PROPSET_MAP](begin-propset-map.md)
#### [BEGIN_PROVIDER_COLUMN_MAP](begin-provider-column-map.md)
#### [BEGIN_SCHEMA_MAP](begin-schema-map.md)
#### [CHAIN_PROPERTY_SET](chain-property-set.md)
#### [END_PROPERTY_SET](end-property-set.md)
#### [END_PROPSET_MAP](end-propset-map.md)
#### [END_PROVIDER_COLUMN_MAP](end-provider-column-map.md)
#### [END_SCHEMA_MAP](end-schema-map.md)
#### [PROVIDER_COLUMN_ENTRY](provider-column-entry.md)
#### [PROVIDER_COLUMN_ENTRY_GN](provider-column-entry-gn.md)
#### [PROVIDER_COLUMN_ENTRY_FIXED](provider-column-entry-fixed.md)
#### [PROVIDER_COLUMN_ENTRY_LENGTH](provider-column-entry-length.md)
#### [PROVIDER_COLUMN_ENTRY_STR](provider-column-entry-str.md)
#### [PROVIDER_COLUMN_ENTRY_TYPE_LENGTH](provider-column-entry-type-length.md)
#### [PROVIDER_COLUMN_ENTRY_WSTR](provider-column-entry-wstr.md)
#### [PROPERTY_INFO_ENTRY](property-info-entry.md)
#### [PROPERTY_INFO_ENTRY_EX](property-info-entry-ex.md)
#### [PROPERTY_INFO_ENTRY_VALUE](property-info-entry-value.md)
#### [SCHEMA_ENTRY](schema-entry.md)
