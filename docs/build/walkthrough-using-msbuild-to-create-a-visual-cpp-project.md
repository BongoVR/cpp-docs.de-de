---
title: 'Exemplarische Vorgehensweise: Verwenden von MSBuild zum Erstellen eines Visual C++-Projekts | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
f1_keywords:
- msbuild.cpp.walkthrough.createproject
dev_langs:
- C++
helpviewer_keywords:
- 'msbuild (c++), walkthrough: create a project'
ms.assetid: 52350d1c-c373-4868-923c-5e8be6f67adb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 88366f78556ebcab6dc7b796cdeeefd402b99721
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="walkthrough-using-msbuild-to-create-a-visual-c-project"></a>Exemplarische Vorgehensweise: Verwenden von MSBuild zum Erstellen eines Visual C++-Projekts
Diese exemplarische Vorgehensweise veranschaulicht, wie [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)] zum Erstellen eines Visual C++-Projekts an der Eingabeaufforderung. Sie erfahren, wie die C++-Quelldateien und eine XML-basierte Projektdatei für eine Visual C++-Konsolenanwendung zu erstellen. Nach der Erstellung des Projekts erfahren Sie, wie der Buildprozess angepasst wird.  
  
 In dieser exemplarischen Vorgehensweise werden die folgenden Aufgaben veranschaulicht:  
  
-   Erstellen der C++-Quelldateien für das Projekt  
  
-   Erstellen der [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)]-XML-Projektdatei  
  
-   Erstellen des Projekts mithilfe von [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)]  
  
-   Anpassen des Projekts mithilfe von [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)]  
  
## <a name="prerequisites"></a>Erforderliche Komponenten  
 Für diese exemplarische Vorgehensweise wird Folgendes benötigt:  
  
-   [!INCLUDE[vs_dev12](../atl-mfc-shared/includes/vs_dev12_md.md)]  
  
-   Allgemeine Kenntnisse des [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)]-Systems.  
  
## <a name="creating-the-c-source-files"></a>Erstellen der C++-Quelldateien  
 In dieser exemplarischen Vorgehensweise erstellen Sie ein Projekt, das eine Quell- und eine Headerdatei besitzt. Die Quelldatei "main.cpp" enthält die Hauptfunktion für die Konsolenanwendung. Die Headerdatei "main.h" enthält Code zum Einschließen der iostream-Headerdatei. Sie können diese C++-Dateien mit [!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] oder einem Text-Editor erstellen.  
  
#### <a name="to-create-the-c-source-files-for-your-project"></a>So erstellen Sie die C++-Quelldateien für das Projekt  
  
1.  Erstellen Sie ein Verzeichnis für das Projekt.  
  
2.  Erstellen Sie eine Datei mit dem Namen "main.cpp", und fügen Sie der Datei den folgenden Code hinzu:  
  
    ```cpp  
    // main.cpp : the application source code.  
    #include <iostream>  
    #include "main.h"  
    int main()  
    {  
       std::cout << "Hello, from MSBuild!\n";  
       return 0;  
    }  
    ```  
  
3.  Erstellen Sie eine Datei mit dem Namen "main.h", und fügen Sie der Datei den folgenden Code hinzu:  
  
    ```hlsl  
    // main.h: the application header code.  
    /* Additional source code to include. */  
    ```  
  
## <a name="creating-the-xml-msbuild-project-file"></a>Erstellen der XML-MSBuild-Projektdatei  
 Ein [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)] Projektdatei ist eine XML-Datei, die ein Projektstammelement enthält (\<Projekt >). Im folgenden Beispielprojekt die \<Projekt >-Element enthält sieben untergeordnete Elemente:  
  
-   Drei Elementgruppentags (\<ItemGroup >), die Projektkonfiguration und Plattform, Quelldateiname und Headerdateiname angeben.  
  
-   Drei importtags (\<Importieren >), die den Speicherort der Microsoft Visual C++-Einstellungen angeben.  
  
-   Ein eigenschaftsgruppentag (\<PropertyGroup >), das projekteinstellungen angibt.  
  
#### <a name="to-create-the-msbuild-project-file"></a>So erstellen Sie die MSBuild-Projektdatei  
  
1.  Verwenden Sie einen Text-Editor So erstellen eine Projektdatei mit dem Namen `myproject.vcxproj`, und fügen Sie dann den folgenden Stamm \<Projekt > Element. Fügen Sie die Elemente in den folgenden Verfahrensschritten zwischen den Stamm \<Projekt > Tags:  
  
    ```xml  
    <Project DefaultTargets="Build" ToolsVersion="12.0" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    </Project>  
    ```  
  
2.  Fügen Sie die folgenden beiden \<ProjectConfiguration > untergeordneten Elemente in einer \<ItemGroup >-Element. Das untergeordnete Element gibt Debug- und Releasekonfigurationen für ein 32-Bit-Windows-Betriebssystem an:  
  
    ```xml  
    <ItemGroup>  
      <ProjectConfiguration Include="Debug|Win32">  
        <Configuration>Debug</Configuration>  
        <Platform>Win32</Platform>  
      </ProjectConfiguration>  
      <ProjectConfiguration Include="Release|Win32">  
        <Configuration>Release</Configuration>  
        <Platform>Win32</Platform>  
      </ProjectConfiguration>  
    </ItemGroup>  
  
    ```  
  
3.  Fügen Sie die folgenden \<Import / >-Element, das den Pfad der standardmäßigen C++-Einstellungen für dieses Projekt angibt:  
  
    ```xml  
    <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />  
  
    ```  
  
4.  Fügen Sie das folgende Eigenschaftengruppenelement (\<PropertyGroup >), das zwei Projekteigenschaften angibt:  
  
    ```xml  
    <PropertyGroup>  
      <ConfigurationType>Application</ConfigurationType>  
      <PlatformToolset>v120</PlatformToolset>  
    </PropertyGroup>  
    ```  
  
5.  Fügen Sie die folgenden \<Import / >-Element, das den Pfad der aktuellen C++-Einstellungen für dieses Projekt angibt:  
  
    ```xml  
    <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />  
    ```  
  
6.  Fügen Sie die folgenden \<ClCompile > untergeordneten Elements in einem \<ItemGroup >-Element. Das untergeordnete Element gibt den Namen der zu kompilierenden C/C++-Quelldatei an:  
  
    ```xml  
    <ItemGroup>  
      <ClCompile Include="main.cpp" />  
    </ItemGroup>  
    ```  
  
7.  Fügen Sie die folgenden \<ClInclude > untergeordneten Elements in einem \<ItemGroup >-Element. Das untergeordnete Element gibt den Namen der Headerdatei für die C/C++-Quelldatei an:  
  
    ```xml  
    <ItemGroup>  
      <ClInclude Include="main.h" />  
    </ItemGroup>  
    ```  
  
8.  Fügen Sie die folgenden \<Import >-Element, das den Pfad der Datei angibt, die das Ziel für dieses Projekt definiert:  
  
    ```xml  
    <Import Project="$(VCTargetsPath)\Microsoft.Cpp.Targets" />  
  
    ```  
  
### <a name="complete-project-file"></a>Vollständige Projektdatei  
 Im folgenden Code wird die zuvor erstellte vollständige Projektdatei dargestellt.  
  
```xml  
<Project DefaultTargets="Build" ToolsVersion="12.0" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  <ItemGroup>  
    <ProjectConfiguration Include="Debug|Win32">  
      <Configuration>Debug</Configuration>  
      <Platform>Win32</Platform>  
    </ProjectConfiguration>  
    <ProjectConfiguration Include="Release|Win32">  
      <Configuration>Release</Configuration>  
      <Platform>Win32</Platform>  
    </ProjectConfiguration>  
  </ItemGroup>  
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />  
  <PropertyGroup>  
    <ConfigurationType>Application</ConfigurationType>  
    <PlatformToolset>v120</PlatformToolset>  
  </PropertyGroup>  
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />  
  <ItemGroup>  
    <ClCompile Include="main.cpp" />  
  </ItemGroup>  
  <ItemGroup>  
    <ClInclude Include="main.h" />  
  </ItemGroup>  
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.Targets" />  
</Project>  
```  
  
## <a name="using-msbuild-to-build-your-project"></a>Verwenden von MSBuild für die Projekterstellung  
 Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, um die Konsolenanwendung zu erstellen:  
  
```  
msbuild myproject.vcxproj /p:configuration=debug  
```  
  
 Von [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)] wird ein Verzeichnis für die Ausgabedateien erstellt, und anschließend wird das Projekt kompiliert und verknüpft, um das Programm "Myproject.exe" zu generieren. Nachdem der Buildprozess beendet wurde, verwenden Sie den folgenden Befehl, um die Anwendung auszuführen:  
  
```  
myproject  
```  
  
 Die Anwendung sollte "Hello, from MSBuild!" angezeigt. im Konsolenfenster anzuzeigen.  
  
## <a name="customizing-your-project"></a>Anpassen des Projekts  
 [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)] ermöglicht die Ausführung von vordefinierten Buildzielen, das Übernehmen von benutzerdefinierten Eigenschaften und das Verwenden benutzerdefinierter Tools, Ereignisse und Buildschritte. In diesem Abschnitt werden die folgenden Aufgaben veranschaulicht:  
  
-   Mithilfe von [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)] mit Buildzielen.  
  
-   Mithilfe von [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)] mit Buildeigenschaften.  
  
-   Verwenden von [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)] mit dem 64-Bit-Compiler und Tools.  
  
-   Verwenden von [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)] mit unterschiedlichen Toolsets  
  
-   Hinzufügen von [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)]-Anpassungen  
  
### <a name="using-msbuild-with-build-targets"></a>Verwenden von MSBuild mit Buildzielen  
 Ein *Buildziel* ist ein benannter Satz von vordefinierten oder benutzerdefinierten Befehlen, die während der Builderstellung ausgeführt werden kann. Verwenden Sie die Zielbefehlszeilenoption (**/t**) um ein Buildziel anzugeben. Im Fall von der `myproject` -Beispielprojekts werden vom vordefinierten **Bereinigen** Ziel alle Dateien im Debugordner gelöscht, und eine neue Protokolldatei erstellt.  
  
 Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, um `myproject` zu bereinigen.  
  
 `msbuild myproject.vcxproj /t:clean`  
  
### <a name="using-msbuild-with-build-properties"></a>Verwenden von MSBuild mit Buildeigenschaften  
 Die Eigenschaften-Befehlszeilenoption (**/p**) ermöglicht es Ihnen, eine Eigenschaft in der Projektbuilddatei zu überschreiben. Im `myproject`- Beispielprojekt wird die Release- oder Debugbuildkonfiguration durch die `Configuration`-Eigenschaft angegeben. Das Betriebssystem, das für die Ausführung der erstellten Anwendung vorgesehen ist, wird durch die `Platform`-Eigenschaft angegeben.  
  
 Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, um einen Debugbuild der `myproject`-Anwendung zu erstellen, die für die Ausführung unter Windows (32 Bit) vorgesehen ist.  
  
 `msbuild myproject.vcxproj /p:configuration=debug /p:platform=win32`  
  
 Angenommen, durch das `myproject`-Beispielprojekt wird auch eine Konfiguration für Windows (64 Bit) und eine andere Konfiguration für ein benutzerdefiniertes Betriebssystem mit dem Namen `myplatform` definiert.  
  
 Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, um einen Releasebuild zu erstellen, der unter Windows (64 Bit) ausgeführt wird.  
  
 `msbuild myproject.vcxproj /p:configuration=release /p:platform=x64`  
  
 Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, um einen Releasebuild für `myplatform` anzuzeigen:  
  
 `msbuild myproject.vcxproj /p:configuration=release /p:platform=myplatform`  
  
### <a name="using-msbuild-with-the-64-bit-compiler-and-tools"></a>Verwenden von MSBuild mit dem 64-Bit-Compiler und Tools  
 Wenn Sie Visual C++ standardmäßig auf 64-Bit-Windows installiert haben, werden die 64-Bit-X64 systemeigene und cross-Tools installiert. Sie können [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)] konfigurieren, um den 64-Bit-Compiler und die Tools zur Erstellung Ihrer Anwendung zu verwenden, indem Sie die `PreferredToolArchitecture`-Eigenschaft festlegen. Diese Eigenschaft beeinflusst nicht die Projektkonfigurations- oder Plattformeigenschaften. Standardmäßig wird die 32-Bit-Version des Tools verwendet. Die 64-Bit-Version des Compilers und der Tools angeben möchten, fügen Sie das folgende Eigenschaftengruppenelement der Projektdatei "MyProject.vcxproj" nach der `Microsoft.Cpp.default.props` \<Import / >-Element:  
  
```xml  
<PropertyGroup>  
    <PreferredToolArchitecture>x64</PreferredToolArchitecture>  
</PropertyGroup>  
```  
  
 Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, um die 64-Bit-Tools zur Erstellung Ihrer Anwendung zu verwenden.  
  
 `msbuild myproject.vcxproj /p:PreferredToolArchitecture=x64`  
  
### <a name="using-msbuild-with-a-different-toolset"></a>Verwenden von MSBuild mit einem anderen Toolset  
 Wenn Sie die Toolsets- und Bibliotheken für andere Versionen von Visual C++ installiert haben, haben [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)] können entweder Anwendungen für die aktuelle Version von Visual C++ erstellen, oder für die anderen installierten Versionen. Wenn Sie installiert haben z. B. [!INCLUDE[cpp_dev11_long](../build/includes/cpp_dev11_long_md.md)], um das Visual C++ 11.0 Toolset für Windows XP anzugeben, fügen Sie das folgende Eigenschaftengruppenelement der Projektdatei "MyProject.vcxproj" nach dem Element "Microsoft.cpp.props" `<Import />` Element:  
  
```xml  
<PropertyGroup>  
    <PlatformToolset>v110_xp</PlatformToolset>  
</PropertyGroup>  
```  
  
 Geben Sie einen der folgenden Befehle an, um Ihr Projekt mit Visual C++ 11.0 Windows XP-Toolset neu zu erstellen:  
  
 `msbuild myproject.vcxproj /p:PlatformToolset=v110_xp /t:rebuild`  
  
 `msbuild myproject.vcxproj /t:rebuild`  
  
### <a name="adding-msbuild-customizations"></a>Hinzufügen von MSBuild-Anpassungen  
 [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)] bietet verschiedene Möglichkeiten zur Anpassung des Buildprozesses. Die folgenden Themen zeigen, wie dem [!INCLUDE[vstecmsbuild](../build/includes/vstecmsbuild_md.md)]-Projekt benutzerdefinierte Buildschritte, Tools und Ereignisse hinzugefügt werden:  
  
-   [Vorgehensweise: Hinzufügen eines benutzerdefinierten Buildschritts zu MSBuild-Projekten](../build/how-to-add-a-custom-build-step-to-msbuild-projects.md)  
  
-   [Vorgehensweise: Hinzufügen von benutzerdefinierten Buildtools zu MSBuild-Projekten](../build/how-to-add-custom-build-tools-to-msbuild-projects.md)  
  
-   [Vorgehensweise: Verwenden von Buildereignissen in MSBuild-Projekten](../build/how-to-use-build-events-in-msbuild-projects.md)