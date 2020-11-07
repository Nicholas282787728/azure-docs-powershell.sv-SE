---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 07ec4223414bbdbab8e3fa4d11641d040d918209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746050"
---
# <span data-ttu-id="e104c-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e104c-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="e104c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e104c-102">SYNOPSIS</span></span>
<span data-ttu-id="e104c-103">Distribuerar ett Azure Web App från en ZIP-, JAR-eller WAR-fil med zipdeploy.</span><span class="sxs-lookup"><span data-stu-id="e104c-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="e104c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e104c-104">SYNTAX</span></span>

### <span data-ttu-id="e104c-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e104c-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e104c-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e104c-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e104c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e104c-107">DESCRIPTION</span></span>
<span data-ttu-id="e104c-108">Cmdleten **Publishing-AzWebApp** laddar upp innehåll till en befintlig Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e104c-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="e104c-109">Innehållet ska paketeras i en ZIP-fil om du använder stackar som .NET, python eller nod, eller en WAR-eller JAR-fil om du använder Java.</span><span class="sxs-lookup"><span data-stu-id="e104c-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="e104c-110">Innehållet bör vara förbyggt och klart att köras utan några ytterligare installations anvisningar under distributionen.</span><span class="sxs-lookup"><span data-stu-id="e104c-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="e104c-111">Denna cmdlet använder funktionerna kudu zipdeploy och wardeploy för distribution av innehåll.</span><span class="sxs-lookup"><span data-stu-id="e104c-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="e104c-112">Se kudu wiki för information om hur zipdeploy och wardeploy fungerar och hur du kan paketera ett webb program för distribution.</span><span class="sxs-lookup"><span data-stu-id="e104c-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="e104c-113"> https://aka.ms/kuduzipdeploy och https://aka.ms/kuduwardeploy innehåller nyttig information om zipdeploy och wardeploy.</span><span class="sxs-lookup"><span data-stu-id="e104c-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="e104c-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e104c-114">EXAMPLES</span></span>

### <span data-ttu-id="e104c-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e104c-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="e104c-116">Överför innehållet i app.zip till webb programmet som heter MyApp som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="e104c-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="e104c-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e104c-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="e104c-118">Uppladdar innehållet i javaproject. War till mellanlagringsområdet för webb programmet som heter ContosoApp som tillhör resurs gruppen ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="e104c-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="e104c-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="e104c-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="e104c-120">Överför innehållet i app.zip till webb programmet som heter ContosoApp som tillhör resurs gruppen ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="e104c-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="e104c-121">Cmdlet körs i ett bakgrunds jobb.</span><span class="sxs-lookup"><span data-stu-id="e104c-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="e104c-122">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="e104c-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```

<span data-ttu-id="e104c-123">Överför innehållet i java_app. jar till webb programmet som heter ContosoApp som tillhör resurs gruppen ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="e104c-123">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="e104c-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e104c-124">PARAMETERS</span></span>

### <span data-ttu-id="e104c-125">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="e104c-125">-ArchivePath</span></span>
<span data-ttu-id="e104c-126">Sökvägen till Arkiv filen.</span><span class="sxs-lookup"><span data-stu-id="e104c-126">The path of the archive file.</span></span> <span data-ttu-id="e104c-127">ZIP, KRIGS och JAR stöds.</span><span class="sxs-lookup"><span data-stu-id="e104c-127">ZIP, WAR, and JAR are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e104c-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e104c-128">-AsJob</span></span>
<span data-ttu-id="e104c-129">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e104c-129">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e104c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e104c-130">-DefaultProfile</span></span>
<span data-ttu-id="e104c-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e104c-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e104c-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="e104c-132">-Name</span></span>
<span data-ttu-id="e104c-133">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="e104c-133">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e104c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e104c-134">-ResourceGroupName</span></span>
<span data-ttu-id="e104c-135">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e104c-135">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e104c-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="e104c-136">-Slot</span></span>
<span data-ttu-id="e104c-137">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="e104c-137">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e104c-138">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e104c-138">-WebApp</span></span>
<span data-ttu-id="e104c-139">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="e104c-139">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e104c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e104c-140">CommonParameters</span></span>
<span data-ttu-id="e104c-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e104c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e104c-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e104c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e104c-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e104c-143">INPUTS</span></span>

### <span data-ttu-id="e104c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e104c-144">System.String</span></span>

### <span data-ttu-id="e104c-145">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e104c-145">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e104c-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e104c-146">OUTPUTS</span></span>

### <span data-ttu-id="e104c-147">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e104c-147">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e104c-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e104c-148">NOTES</span></span>

## <span data-ttu-id="e104c-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e104c-149">RELATED LINKS</span></span>
