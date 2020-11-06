---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 4948de891815345efdc0b3f4ec39fb1874e510b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585264"
---
# <span data-ttu-id="d124f-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d124f-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="d124f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d124f-102">SYNOPSIS</span></span>
<span data-ttu-id="d124f-103">Skapar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d124f-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d124f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d124f-104">SYNTAX</span></span>

### <span data-ttu-id="d124f-105">S1 (standard)</span><span class="sxs-lookup"><span data-stu-id="d124f-105">S1 (Default)</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileId] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d124f-106">S2</span><span class="sxs-lookup"><span data-stu-id="d124f-106">S2</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileName] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d124f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d124f-107">DESCRIPTION</span></span>
<span data-ttu-id="d124f-108">Cmdleten **New-AzureRmWebApp** skapar ett Azure Web App i en given resurs grupp som använder den angivna App Service-abonnemanget och data centret.</span><span class="sxs-lookup"><span data-stu-id="d124f-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="d124f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d124f-109">EXAMPLES</span></span>

### <span data-ttu-id="d124f-110">Exempel 1: skapa ett webb program</span><span class="sxs-lookup"><span data-stu-id="d124f-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="d124f-111">Det här kommandot skapar ett Azure Web App-objekt med namnet ContosoSite i den befintliga resurs gruppen som heter default-West-väster in data Center.</span><span class="sxs-lookup"><span data-stu-id="d124f-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="d124f-112">Kommandot använder en befintlig App Service-plan med namnet ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d124f-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="d124f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d124f-113">PARAMETERS</span></span>

### <span data-ttu-id="d124f-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d124f-114">-AppServicePlan</span></span>
<span data-ttu-id="d124f-115">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="d124f-115">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="d124f-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="d124f-117">Program inställningar åsidosätter hash</span><span class="sxs-lookup"><span data-stu-id="d124f-117">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="d124f-118">-AseName</span></span>
<span data-ttu-id="d124f-119">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="d124f-119">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d124f-120">-AseResourceGroupName</span></span>
<span data-ttu-id="d124f-121">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="d124f-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="d124f-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="d124f-123">Ignorera anpassade värd namns alternativ</span><span class="sxs-lookup"><span data-stu-id="d124f-123">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="d124f-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="d124f-125">Alternativet Ignorera käll kontroll</span><span class="sxs-lookup"><span data-stu-id="d124f-125">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-126">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="d124f-126">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="d124f-127">Inkludera alternativet Source WebApp-fack</span><span class="sxs-lookup"><span data-stu-id="d124f-127">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="d124f-128">-Location</span></span>
<span data-ttu-id="d124f-129">Plats</span><span class="sxs-lookup"><span data-stu-id="d124f-129">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="d124f-130">-Name</span></span>
<span data-ttu-id="d124f-131">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d124f-131">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d124f-132">-ResourceGroupName</span></span>
<span data-ttu-id="d124f-133">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d124f-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-134">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="d124f-134">-SourceWebApp</span></span>
<span data-ttu-id="d124f-135">Source WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="d124f-135">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-136">-TrafficManagerProfileId</span><span class="sxs-lookup"><span data-stu-id="d124f-136">-TrafficManagerProfileId</span></span>
<span data-ttu-id="d124f-137">Profil-ID för Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="d124f-137">Traffic Manager Profile Id</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-138">-TrafficManagerProfileName</span><span class="sxs-lookup"><span data-stu-id="d124f-138">-TrafficManagerProfileName</span></span>
<span data-ttu-id="d124f-139">Profil namn för Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="d124f-139">Traffic Manager Profile Name</span></span>

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d124f-140">-DefaultProfile</span></span>
<span data-ttu-id="d124f-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d124f-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d124f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d124f-142">CommonParameters</span></span>
<span data-ttu-id="d124f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d124f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d124f-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d124f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d124f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d124f-145">INPUTS</span></span>

### <span data-ttu-id="d124f-146">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="d124f-146">Site</span></span>
<span data-ttu-id="d124f-147">Parametern ' SourceWebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d124f-147">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d124f-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d124f-148">OUTPUTS</span></span>

## <span data-ttu-id="d124f-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d124f-149">NOTES</span></span>

## <span data-ttu-id="d124f-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d124f-150">RELATED LINKS</span></span>

[<span data-ttu-id="d124f-151">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d124f-151">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="d124f-152">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d124f-152">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="d124f-153">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d124f-153">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="d124f-154">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d124f-154">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="d124f-155">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d124f-155">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


