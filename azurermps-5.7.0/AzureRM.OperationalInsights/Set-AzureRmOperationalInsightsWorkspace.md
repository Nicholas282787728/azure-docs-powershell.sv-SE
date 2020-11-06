---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: a4584e4c0fc64920fbffb7e3d685a9be3ac04ad1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576479"
---
# <span data-ttu-id="8377b-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8377b-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="8377b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8377b-102">SYNOPSIS</span></span>
<span data-ttu-id="8377b-103">Uppdaterar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="8377b-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8377b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8377b-104">SYNTAX</span></span>

### <span data-ttu-id="8377b-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="8377b-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8377b-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="8377b-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8377b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8377b-107">DESCRIPTION</span></span>
<span data-ttu-id="8377b-108">Cmdleten **set-AzureRmOperationalInsightsWorkspace** ändrar arbets ytans konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8377b-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="8377b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8377b-109">EXAMPLES</span></span>

### <span data-ttu-id="8377b-110">Exempel 1: ändra en arbets yta efter namn</span><span class="sxs-lookup"><span data-stu-id="8377b-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="8377b-111">Det här kommandot ändrar SKU och taggar för arbets ytan med namnet min arbets yta i resurs gruppen som heter ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8377b-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8377b-112">Exempel 2: uppdatera en arbets yta med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="8377b-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="8377b-113">Det här kommandot använder cmdleten Get-AzureRmOperationalInsightsWorkspace för att hämta arbets ytan som heter min arbets yta och skickar den till cmdleten **set-AzureRmOperationalInsightsWorkspace** genom att använda pipeline-operatorn för att ange SKU till Premium.</span><span class="sxs-lookup"><span data-stu-id="8377b-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="8377b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8377b-114">PARAMETERS</span></span>

### <span data-ttu-id="8377b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8377b-115">-DefaultProfile</span></span>
<span data-ttu-id="8377b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8377b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8377b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="8377b-117">-Name</span></span>
<span data-ttu-id="8377b-118">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="8377b-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8377b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8377b-119">-ResourceGroupName</span></span>
<span data-ttu-id="8377b-120">Anger namnet på Azure Resource-gruppen.</span><span class="sxs-lookup"><span data-stu-id="8377b-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8377b-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8377b-121">-RetentionInDays</span></span>
<span data-ttu-id="8377b-122">Arbets ytans data lagring i dagar.</span><span class="sxs-lookup"><span data-stu-id="8377b-122">The workspace data retention in days.</span></span> <span data-ttu-id="8377b-123">730 dagar är det högsta tillåtna antalet för alla andra SKU: er</span><span class="sxs-lookup"><span data-stu-id="8377b-123">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8377b-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="8377b-124">-Sku</span></span>
<span data-ttu-id="8377b-125">Anger arbets ytans tjänste nivå.</span><span class="sxs-lookup"><span data-stu-id="8377b-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="8377b-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="8377b-126">Valid values are:</span></span> 

- <span data-ttu-id="8377b-127">gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="8377b-127">free</span></span>
- <span data-ttu-id="8377b-128">standar</span><span class="sxs-lookup"><span data-stu-id="8377b-128">standard</span></span>
- <span data-ttu-id="8377b-129">Beta</span><span class="sxs-lookup"><span data-stu-id="8377b-129">premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8377b-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8377b-130">-Tag</span></span>
<span data-ttu-id="8377b-131">Resurs märkningen för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="8377b-131">The resource tags for the workspace.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8377b-132">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="8377b-132">-Workspace</span></span>
<span data-ttu-id="8377b-133">Anger arbets ytan som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8377b-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8377b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8377b-134">CommonParameters</span></span>
<span data-ttu-id="8377b-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8377b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8377b-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8377b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8377b-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8377b-137">INPUTS</span></span>

### <span data-ttu-id="8377b-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8377b-138">PSWorkspace</span></span>
<span data-ttu-id="8377b-139">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="8377b-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="8377b-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8377b-140">OUTPUTS</span></span>

### <span data-ttu-id="8377b-141">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8377b-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="8377b-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8377b-142">NOTES</span></span>

## <span data-ttu-id="8377b-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8377b-143">RELATED LINKS</span></span>

[<span data-ttu-id="8377b-144">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="8377b-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="8377b-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8377b-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


