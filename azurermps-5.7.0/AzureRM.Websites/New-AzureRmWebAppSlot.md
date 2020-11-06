---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: a3ae7f879827b7b260e60f0d3e0aa70e5a6ab533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575413"
---
# <span data-ttu-id="90b0d-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="90b0d-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="90b0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="90b0d-103">Skapar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="90b0d-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90b0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90b0d-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90b0d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90b0d-105">DESCRIPTION</span></span>
<span data-ttu-id="90b0d-106">Cmdleten **New-AzureRmWebAppSlot** skapar en Azure Web App-plats i en given resurs grupp som använder den angivna App Service-abonnemanget och data centret.</span><span class="sxs-lookup"><span data-stu-id="90b0d-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="90b0d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90b0d-107">EXAMPLES</span></span>

### <span data-ttu-id="90b0d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="90b0d-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="90b0d-109">Det här kommandot skapar en kort plats med namnet Slot001 under ett befintligt webbprogram-namn ContosoSite i den befintliga resurs gruppen med namnet default-Web-West i Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="90b0d-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="90b0d-110">Kommandot använder en befintlig App Service-plan med namnet ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="90b0d-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="90b0d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90b0d-111">PARAMETERS</span></span>

### <span data-ttu-id="90b0d-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="90b0d-112">-AppServicePlan</span></span>
<span data-ttu-id="90b0d-113">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="90b0d-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="90b0d-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="90b0d-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="90b0d-115">Program inställningar åsidosätter hash</span><span class="sxs-lookup"><span data-stu-id="90b0d-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b0d-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="90b0d-116">-AseName</span></span>
<span data-ttu-id="90b0d-117">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="90b0d-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b0d-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b0d-118">-AseResourceGroupName</span></span>
<span data-ttu-id="90b0d-119">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="90b0d-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b0d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b0d-120">-DefaultProfile</span></span>
<span data-ttu-id="90b0d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90b0d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90b0d-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="90b0d-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="90b0d-123">Alternativet Ignorera anpassade värd namn</span><span class="sxs-lookup"><span data-stu-id="90b0d-123">Ignore Custom HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b0d-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="90b0d-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="90b0d-125">Alternativet Ignorera käll kontroll</span><span class="sxs-lookup"><span data-stu-id="90b0d-125">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b0d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="90b0d-126">-Name</span></span>
<span data-ttu-id="90b0d-127">Webapp-namn</span><span class="sxs-lookup"><span data-stu-id="90b0d-127">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b0d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b0d-128">-ResourceGroupName</span></span>
<span data-ttu-id="90b0d-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="90b0d-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b0d-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="90b0d-130">-Slot</span></span>
<span data-ttu-id="90b0d-131">Webapp-slot</span><span class="sxs-lookup"><span data-stu-id="90b0d-131">Webapp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b0d-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="90b0d-132">-SourceWebApp</span></span>
<span data-ttu-id="90b0d-133">Source WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="90b0d-133">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90b0d-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90b0d-134">-AsJob</span></span>
<span data-ttu-id="90b0d-135">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="90b0d-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90b0d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b0d-136">CommonParameters</span></span>
<span data-ttu-id="90b0d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90b0d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b0d-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90b0d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b0d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90b0d-139">INPUTS</span></span>

### <span data-ttu-id="90b0d-140">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="90b0d-140">Site</span></span>
<span data-ttu-id="90b0d-141">Parametern ' SourceWebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="90b0d-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="90b0d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90b0d-142">OUTPUTS</span></span>

## <span data-ttu-id="90b0d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90b0d-143">NOTES</span></span>

## <span data-ttu-id="90b0d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90b0d-144">RELATED LINKS</span></span>

[<span data-ttu-id="90b0d-145">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="90b0d-145">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="90b0d-146">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="90b0d-146">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="90b0d-147">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="90b0d-147">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="90b0d-148">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="90b0d-148">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="90b0d-149">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="90b0d-149">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="90b0d-150">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="90b0d-150">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="90b0d-151">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="90b0d-151">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="90b0d-152">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="90b0d-152">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
