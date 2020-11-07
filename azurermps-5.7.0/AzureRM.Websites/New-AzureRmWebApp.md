---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 05ee02fcb1a1f03c2a9b349754009a178a1668b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580915"
---
# <span data-ttu-id="0cb0f-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb0f-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="0cb0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0cb0f-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb0f-103">Skapar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0cb0f-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cb0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0cb0f-104">SYNTAX</span></span>

### <span data-ttu-id="0cb0f-105">SimpleParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0cb0f-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cb0f-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cb0f-106">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cb0f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0cb0f-107">DESCRIPTION</span></span>
<span data-ttu-id="0cb0f-108">Cmdleten **New-AzureRmWebApp** skapar ett Azure Web App i en given resurs grupp som använder den angivna App Service-abonnemanget och data centret.</span><span class="sxs-lookup"><span data-stu-id="0cb0f-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="0cb0f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0cb0f-109">EXAMPLES</span></span>

### <span data-ttu-id="0cb0f-110">Exempel 1: skapa ett webb program</span><span class="sxs-lookup"><span data-stu-id="0cb0f-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="0cb0f-111">Det här kommandot skapar ett Azure Web App-objekt med namnet ContosoSite i den befintliga resurs gruppen som heter default-West-väster in data Center.</span><span class="sxs-lookup"><span data-stu-id="0cb0f-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="0cb0f-112">Kommandot använder en befintlig App Service-plan med namnet ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="0cb0f-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="0cb0f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0cb0f-113">PARAMETERS</span></span>

### <span data-ttu-id="0cb0f-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0cb0f-114">-AppServicePlan</span></span>
<span data-ttu-id="0cb0f-115">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="0cb0f-115">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="0cb0f-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="0cb0f-117">Program inställningar åsidosätter hash</span><span class="sxs-lookup"><span data-stu-id="0cb0f-117">App Settings Overrides HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="0cb0f-118">-AseName</span></span>
<span data-ttu-id="0cb0f-119">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="0cb0f-119">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cb0f-120">-AseResourceGroupName</span></span>
<span data-ttu-id="0cb0f-121">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="0cb0f-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cb0f-122">-AsJob</span></span>
<span data-ttu-id="0cb0f-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0cb0f-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb0f-124">-DefaultProfile</span></span>
<span data-ttu-id="0cb0f-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0cb0f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="0cb0f-126">-GitRepositoryPath</span></span>
<span data-ttu-id="0cb0f-127">Sökvägen till GitHub-databasen containign webb programmet som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="0cb0f-127">Path to the GitHub repository containign the web application to deploy.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="0cb0f-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="0cb0f-129">Ignorera anpassade värd namns alternativ</span><span class="sxs-lookup"><span data-stu-id="0cb0f-129">Ignore Custom Host Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="0cb0f-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="0cb0f-131">Alternativet Ignorera käll kontroll</span><span class="sxs-lookup"><span data-stu-id="0cb0f-131">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-132">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="0cb0f-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="0cb0f-133">Inkludera alternativet Source WebApp-fack</span><span class="sxs-lookup"><span data-stu-id="0cb0f-133">Include Source WebApp Slots Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="0cb0f-134">-Location</span></span>
<span data-ttu-id="0cb0f-135">Plats</span><span class="sxs-lookup"><span data-stu-id="0cb0f-135">Location</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="0cb0f-136">-Name</span></span>
<span data-ttu-id="0cb0f-137">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="0cb0f-137">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cb0f-138">-ResourceGroupName</span></span>
<span data-ttu-id="0cb0f-139">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0cb0f-139">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb0f-140">-SourceWebApp</span></span>
<span data-ttu-id="0cb0f-141">Source WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="0cb0f-141">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0cb0f-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="0cb0f-143">Resurs-ID för befintlig Traffic Manager-profil</span><span class="sxs-lookup"><span data-stu-id="0cb0f-143">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0cb0f-144">-Confirm</span></span>
<span data-ttu-id="0cb0f-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0cb0f-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cb0f-146">-WhatIf</span></span>
<span data-ttu-id="0cb0f-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0cb0f-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0cb0f-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0cb0f-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb0f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb0f-149">CommonParameters</span></span>
<span data-ttu-id="0cb0f-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cb0f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb0f-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cb0f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb0f-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0cb0f-152">INPUTS</span></span>

### <span data-ttu-id="0cb0f-153">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="0cb0f-153">Site</span></span>
<span data-ttu-id="0cb0f-154">Parametern ' SourceWebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0cb0f-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0cb0f-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0cb0f-155">OUTPUTS</span></span>

### <span data-ttu-id="0cb0f-156">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="0cb0f-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="0cb0f-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0cb0f-157">NOTES</span></span>

## <span data-ttu-id="0cb0f-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0cb0f-158">RELATED LINKS</span></span>

[<span data-ttu-id="0cb0f-159">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb0f-159">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="0cb0f-160">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb0f-160">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="0cb0f-161">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb0f-161">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="0cb0f-162">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb0f-162">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="0cb0f-163">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0cb0f-163">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)

