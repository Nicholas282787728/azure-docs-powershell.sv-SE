---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 3e886803ff608522bd2d563dd9b6cd6effcfe074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585248"
---
# <span data-ttu-id="3e3b9-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e3b9-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="3e3b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e3b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3e3b9-103">Skapar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e3b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e3b9-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e3b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e3b9-105">DESCRIPTION</span></span>
<span data-ttu-id="3e3b9-106">Cmdleten **New-AzureRmWebAppSlot** skapar en Azure Web App-plats i en given resurs grupp som använder den angivna App Service-abonnemanget och data centret.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="3e3b9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e3b9-107">EXAMPLES</span></span>

### <span data-ttu-id="3e3b9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e3b9-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="3e3b9-109">Det här kommandot skapar en kort plats med namnet Slot001 under ett befintligt webbprogram-namn ContosoSite i den befintliga resurs gruppen med namnet default-Web-West i Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="3e3b9-110">Kommandot använder en befintlig App Service-plan med namnet ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="3e3b9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e3b9-111">PARAMETERS</span></span>

### <span data-ttu-id="3e3b9-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3e3b9-112">-AppServicePlan</span></span>
<span data-ttu-id="3e3b9-113">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="3e3b9-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="3e3b9-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="3e3b9-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="3e3b9-115">Program inställningar åsidosätter hash</span><span class="sxs-lookup"><span data-stu-id="3e3b9-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="3e3b9-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="3e3b9-116">-AseName</span></span>
<span data-ttu-id="3e3b9-117">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="3e3b9-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="3e3b9-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e3b9-118">-AseResourceGroupName</span></span>
<span data-ttu-id="3e3b9-119">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="3e3b9-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="3e3b9-120">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="3e3b9-120">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="3e3b9-121">Alternativet Ignorera anpassade värd namn</span><span class="sxs-lookup"><span data-stu-id="3e3b9-121">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="3e3b9-122">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="3e3b9-122">-IgnoreSourceControl</span></span>
<span data-ttu-id="3e3b9-123">Alternativet Ignorera käll kontroll</span><span class="sxs-lookup"><span data-stu-id="3e3b9-123">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="3e3b9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e3b9-124">-Name</span></span>
<span data-ttu-id="3e3b9-125">Webapp-namn</span><span class="sxs-lookup"><span data-stu-id="3e3b9-125">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e3b9-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e3b9-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="3e3b9-127">Resource Group Name</span></span>

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

### <span data-ttu-id="3e3b9-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="3e3b9-128">-Slot</span></span>
<span data-ttu-id="3e3b9-129">Webapp-slot</span><span class="sxs-lookup"><span data-stu-id="3e3b9-129">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b9-130">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="3e3b9-130">-SourceWebApp</span></span>
<span data-ttu-id="3e3b9-131">Source WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="3e3b9-131">Source WebApp Object</span></span>

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

### <span data-ttu-id="3e3b9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e3b9-132">-DefaultProfile</span></span>
<span data-ttu-id="3e3b9-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e3b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e3b9-134">CommonParameters</span></span>
<span data-ttu-id="3e3b9-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e3b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e3b9-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e3b9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e3b9-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e3b9-137">INPUTS</span></span>

### <span data-ttu-id="3e3b9-138">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="3e3b9-138">Site</span></span>
<span data-ttu-id="3e3b9-139">Parametern ' SourceWebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3e3b9-139">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3e3b9-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e3b9-140">OUTPUTS</span></span>

## <span data-ttu-id="3e3b9-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e3b9-141">NOTES</span></span>

## <span data-ttu-id="3e3b9-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e3b9-142">RELATED LINKS</span></span>

[<span data-ttu-id="3e3b9-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e3b9-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="3e3b9-144">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e3b9-144">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="3e3b9-145">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e3b9-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="3e3b9-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e3b9-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="3e3b9-147">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e3b9-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="3e3b9-148">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3e3b9-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="3e3b9-149">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3e3b9-149">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="3e3b9-150">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e3b9-150">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
