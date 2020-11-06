---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 56cf34fce43465594a0a8862194bb15b117dda6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573412"
---
# <span data-ttu-id="35ac7-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="35ac7-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="35ac7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="35ac7-103">Skapar en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="35ac7-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35ac7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35ac7-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35ac7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35ac7-105">DESCRIPTION</span></span>
<span data-ttu-id="35ac7-106">Cmdleten **New-AzureRmPowerBIWorkspaceCollection** skapar en Power BI-arbetsyta för din Azure-prenumeration i angiven resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="35ac7-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="35ac7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35ac7-107">EXAMPLES</span></span>

### <span data-ttu-id="35ac7-108">Exempel 1: skapa en samling med arbets ytor</span><span class="sxs-lookup"><span data-stu-id="35ac7-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="35ac7-109">Det här kommandot skapar en arbets yta med namnet WCN11 i den angivna resurs gruppen på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="35ac7-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="35ac7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35ac7-110">PARAMETERS</span></span>

### <span data-ttu-id="35ac7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ac7-111">-DefaultProfile</span></span>
<span data-ttu-id="35ac7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="35ac7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35ac7-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="35ac7-113">-Location</span></span>
<span data-ttu-id="35ac7-114">Anger den Azure-plats där den här cmdleten skapar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="35ac7-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35ac7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ac7-115">-ResourceGroupName</span></span>
<span data-ttu-id="35ac7-116">Anger namnet på den resurs grupp som den här cmdleten skapar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="35ac7-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35ac7-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="35ac7-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="35ac7-118">Anger ett namn för Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="35ac7-118">Specifies a name for the Power BI workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35ac7-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35ac7-119">-Confirm</span></span>
<span data-ttu-id="35ac7-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35ac7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ac7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ac7-121">-WhatIf</span></span>
<span data-ttu-id="35ac7-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35ac7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35ac7-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35ac7-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ac7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ac7-124">CommonParameters</span></span>
<span data-ttu-id="35ac7-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ac7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ac7-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ac7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ac7-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35ac7-127">INPUTS</span></span>

### <span data-ttu-id="35ac7-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="35ac7-128">None</span></span>
<span data-ttu-id="35ac7-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="35ac7-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35ac7-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35ac7-130">OUTPUTS</span></span>

### <span data-ttu-id="35ac7-131">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="35ac7-131">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="35ac7-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35ac7-132">NOTES</span></span>

## <span data-ttu-id="35ac7-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35ac7-133">RELATED LINKS</span></span>

[<span data-ttu-id="35ac7-134">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="35ac7-134">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="35ac7-135">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="35ac7-135">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


