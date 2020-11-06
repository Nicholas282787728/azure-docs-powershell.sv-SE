---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 766682df23beaa7c513ff54554a3ebd59a6d1537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584599"
---
# <span data-ttu-id="4e6d4-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4e6d4-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="4e6d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e6d4-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6d4-103">Återställer den angivna åtkomst tangenten.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e6d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e6d4-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e6d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e6d4-105">DESCRIPTION</span></span>
<span data-ttu-id="4e6d4-106">Cmdleten **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** återställer den angivna åtkomst tangenten i din Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="4e6d4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e6d4-107">EXAMPLES</span></span>

### <span data-ttu-id="4e6d4-108">Exempel 1: Återställ primär åtkomst-tangenten</span><span class="sxs-lookup"><span data-stu-id="4e6d4-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="4e6d4-109">Det här kommandot återställer den primära åtkomst-tangenten för arbets ytan med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="4e6d4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e6d4-110">PARAMETERS</span></span>

### <span data-ttu-id="4e6d4-111">-Key1</span><span class="sxs-lookup"><span data-stu-id="4e6d4-111">-Key1</span></span>
<span data-ttu-id="4e6d4-112">Anger att denna cmdlet återställer primär åtkomst-tangenten.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-112">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="4e6d4-113">-Key2</span><span class="sxs-lookup"><span data-stu-id="4e6d4-113">-Key2</span></span>
<span data-ttu-id="4e6d4-114">Anger att denna cmdlet återställer den sekundära åtkomst-tangenten.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-114">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="4e6d4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e6d4-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e6d4-116">Anger namnet på samlingens resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-116">Specifies the name of the resource group of the collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d4-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="4e6d4-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="4e6d4-118">Anger namnet på den Power BI-arbetsyta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-118">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d4-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e6d4-119">-Confirm</span></span>
<span data-ttu-id="4e6d4-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e6d4-121">-WhatIf</span></span>
<span data-ttu-id="4e6d4-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e6d4-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6d4-124">-DefaultProfile</span></span>
<span data-ttu-id="4e6d4-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e6d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6d4-126">CommonParameters</span></span>
<span data-ttu-id="4e6d4-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e6d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6d4-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e6d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6d4-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e6d4-129">INPUTS</span></span>

## <span data-ttu-id="4e6d4-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e6d4-130">OUTPUTS</span></span>

### <span data-ttu-id="4e6d4-131">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="4e6d4-131">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="4e6d4-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e6d4-132">NOTES</span></span>

## <span data-ttu-id="4e6d4-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e6d4-133">RELATED LINKS</span></span>

[<span data-ttu-id="4e6d4-134">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4e6d4-134">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


