---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272492"
---
# <span data-ttu-id="b4bbb-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b4bbb-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="b4bbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bbb-103">Distribuerar ett Azure Web App från en ZIP-, JAR-eller WAR-fil med zipdeploy.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="b4bbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4bbb-104">SYNTAX</span></span>

### <span data-ttu-id="b4bbb-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b4bbb-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4bbb-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b4bbb-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="b4bbb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4bbb-107">DESCRIPTION</span></span>
<span data-ttu-id="b4bbb-108">Cmdleten **Publishing-AzWebApp** laddar upp innehåll till en befintlig Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="b4bbb-109">Innehållet ska paketeras i en ZIP-fil om du använder stackar som .NET, python eller nod, eller en WAR-eller JAR-fil om du använder Java.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="b4bbb-110">Innehållet bör vara förbyggt och klart att köras utan några ytterligare installations anvisningar under distributionen.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="b4bbb-111">Denna cmdlet använder funktionerna kudu zipdeploy och wardeploy för distribution av innehåll.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="b4bbb-112">Se kudu wiki för information om hur zipdeploy och wardeploy fungerar och hur du kan paketera ett webb program för distribution.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="b4bbb-113"> https://aka.ms/kuduzipdeploy och https://aka.ms/kuduwardeploy innehåller nyttig information om zipdeploy och wardeploy.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="b4bbb-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4bbb-114">EXAMPLES</span></span>

### <span data-ttu-id="b4bbb-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4bbb-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="b4bbb-116">Överför innehållet i app.zip till webb programmet som heter MyApp som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="b4bbb-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b4bbb-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="b4bbb-118">Uppladdar innehållet i javaproject. War till mellanlagringsområdet för webb programmet som heter ContosoApp som tillhör resurs gruppen ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="b4bbb-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="b4bbb-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="b4bbb-120">Överför innehållet i app.zip till webb programmet som heter ContosoApp som tillhör resurs gruppen ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="b4bbb-121">Cmdlet körs i ett bakgrunds jobb.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="b4bbb-122">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="b4bbb-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="b4bbb-123">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="b4bbb-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="b4bbb-124">Överför innehållet i java_app. jar till webb programmet som heter ContosoApp som tillhör resurs gruppen ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="b4bbb-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4bbb-125">PARAMETERS</span></span>

### <span data-ttu-id="b4bbb-126">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="b4bbb-126">-ArchivePath</span></span>
<span data-ttu-id="b4bbb-127">Sökvägen till Arkiv filen.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-127">The path of the archive file.</span></span> <span data-ttu-id="b4bbb-128">ZIP, KRIGS och JAR stöds.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-128">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="b4bbb-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4bbb-129">-AsJob</span></span>
<span data-ttu-id="b4bbb-130">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b4bbb-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4bbb-131">-Force</span><span class="sxs-lookup"><span data-stu-id="b4bbb-131">-Force</span></span>
<span data-ttu-id="b4bbb-132">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="b4bbb-132">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="b4bbb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bbb-133">-DefaultProfile</span></span>
<span data-ttu-id="b4bbb-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4bbb-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4bbb-135">-Name</span></span>
<span data-ttu-id="b4bbb-136">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-136">The name of the web app.</span></span>

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

### <span data-ttu-id="b4bbb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4bbb-137">-ResourceGroupName</span></span>
<span data-ttu-id="b4bbb-138">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-138">The name of the resource group.</span></span>

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

### <span data-ttu-id="b4bbb-139">-Plats</span><span class="sxs-lookup"><span data-stu-id="b4bbb-139">-Slot</span></span>
<span data-ttu-id="b4bbb-140">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-140">The name of the web app slot.</span></span>

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

### <span data-ttu-id="b4bbb-141">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b4bbb-141">-WebApp</span></span>
<span data-ttu-id="b4bbb-142">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="b4bbb-142">The web app object</span></span>

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

### <span data-ttu-id="b4bbb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bbb-143">CommonParameters</span></span>
<span data-ttu-id="b4bbb-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bbb-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4bbb-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bbb-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4bbb-146">INPUTS</span></span>

### <span data-ttu-id="b4bbb-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b4bbb-147">System.String</span></span>

### <span data-ttu-id="b4bbb-148">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="b4bbb-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b4bbb-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4bbb-149">OUTPUTS</span></span>

### <span data-ttu-id="b4bbb-150">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="b4bbb-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b4bbb-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4bbb-151">NOTES</span></span>

## <span data-ttu-id="b4bbb-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4bbb-152">RELATED LINKS</span></span>