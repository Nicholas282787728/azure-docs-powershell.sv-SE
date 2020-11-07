---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7f3a48db5d8f1e6c7b4b0e73b705fc375a0b514f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757249"
---
# <span data-ttu-id="657c4-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="657c4-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="657c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="657c4-102">SYNOPSIS</span></span>
<span data-ttu-id="657c4-103">Tar bort en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="657c4-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="657c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="657c4-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="657c4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="657c4-105">DESCRIPTION</span></span>
<span data-ttu-id="657c4-106">Cmdleten **Remove-AzureRmPowerBIWorkspaceCollection** tar bort en Power BI-arbetsyta från din Azure-prenumeration och resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="657c4-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="657c4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="657c4-107">EXAMPLES</span></span>

### <span data-ttu-id="657c4-108">Exempel 1: ta bort en samling med arbets ytor</span><span class="sxs-lookup"><span data-stu-id="657c4-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="657c4-109">Det här kommandot tar bort arbets ytans samling med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="657c4-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="657c4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="657c4-110">PARAMETERS</span></span>

### <span data-ttu-id="657c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="657c4-111">-DefaultProfile</span></span>
<span data-ttu-id="657c4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="657c4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="657c4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="657c4-113">-ResourceGroupName</span></span>
<span data-ttu-id="657c4-114">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="657c4-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="657c4-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="657c4-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="657c4-116">Anger namnet på den Power BI-arbetsyta som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="657c4-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="657c4-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="657c4-117">-Confirm</span></span>
<span data-ttu-id="657c4-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="657c4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="657c4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="657c4-119">-WhatIf</span></span>
<span data-ttu-id="657c4-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="657c4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="657c4-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="657c4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="657c4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="657c4-122">CommonParameters</span></span>
<span data-ttu-id="657c4-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="657c4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="657c4-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="657c4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="657c4-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="657c4-125">INPUTS</span></span>

### <span data-ttu-id="657c4-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="657c4-126">None</span></span>
<span data-ttu-id="657c4-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="657c4-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="657c4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="657c4-128">OUTPUTS</span></span>

## <span data-ttu-id="657c4-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="657c4-129">NOTES</span></span>

## <span data-ttu-id="657c4-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="657c4-130">RELATED LINKS</span></span>

[<span data-ttu-id="657c4-131">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="657c4-131">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="657c4-132">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="657c4-132">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


