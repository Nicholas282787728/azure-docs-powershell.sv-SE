---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/reset-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 99a575d4eb17cc41eeea49f1db2a801bb6a28c98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573411"
---
# <span data-ttu-id="2be6b-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2be6b-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="2be6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2be6b-102">SYNOPSIS</span></span>
<span data-ttu-id="2be6b-103">Återställer den angivna åtkomst tangenten.</span><span class="sxs-lookup"><span data-stu-id="2be6b-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2be6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2be6b-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2be6b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2be6b-105">DESCRIPTION</span></span>
<span data-ttu-id="2be6b-106">Cmdleten **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** återställer den angivna åtkomst tangenten i din Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="2be6b-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="2be6b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2be6b-107">EXAMPLES</span></span>

### <span data-ttu-id="2be6b-108">Exempel 1: Återställ primär åtkomst-tangenten</span><span class="sxs-lookup"><span data-stu-id="2be6b-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="2be6b-109">Det här kommandot återställer den primära åtkomst-tangenten för arbets ytan med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2be6b-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="2be6b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2be6b-110">PARAMETERS</span></span>

### <span data-ttu-id="2be6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be6b-111">-DefaultProfile</span></span>
<span data-ttu-id="2be6b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2be6b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2be6b-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="2be6b-113">-Key1</span></span>
<span data-ttu-id="2be6b-114">Anger att denna cmdlet återställer primär åtkomst-tangenten.</span><span class="sxs-lookup"><span data-stu-id="2be6b-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="2be6b-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="2be6b-115">-Key2</span></span>
<span data-ttu-id="2be6b-116">Anger att denna cmdlet återställer den sekundära åtkomst-tangenten.</span><span class="sxs-lookup"><span data-stu-id="2be6b-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="2be6b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be6b-117">-ResourceGroupName</span></span>
<span data-ttu-id="2be6b-118">Anger namnet på samlingens resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2be6b-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="2be6b-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="2be6b-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="2be6b-120">Anger namnet på den Power BI-arbetsyta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2be6b-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2be6b-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2be6b-121">-Confirm</span></span>
<span data-ttu-id="2be6b-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2be6b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2be6b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2be6b-123">-WhatIf</span></span>
<span data-ttu-id="2be6b-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2be6b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2be6b-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2be6b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2be6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be6b-126">CommonParameters</span></span>
<span data-ttu-id="2be6b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2be6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be6b-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2be6b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be6b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2be6b-129">INPUTS</span></span>

### <span data-ttu-id="2be6b-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="2be6b-130">None</span></span>
<span data-ttu-id="2be6b-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2be6b-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2be6b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2be6b-132">OUTPUTS</span></span>

### <span data-ttu-id="2be6b-133">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="2be6b-133">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="2be6b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2be6b-134">NOTES</span></span>

## <span data-ttu-id="2be6b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2be6b-135">RELATED LINKS</span></span>

[<span data-ttu-id="2be6b-136">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2be6b-136">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


