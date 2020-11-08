---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 557b1b7c5c2a91ec5e77729e70d2aa58f696d212
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088350"
---
# <span data-ttu-id="0bc20-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0bc20-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="0bc20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0bc20-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc20-103">Skapar en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="0bc20-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="0bc20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0bc20-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bc20-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0bc20-105">DESCRIPTION</span></span>
<span data-ttu-id="0bc20-106">Cmdleten **New-AzPowerBIWorkspaceCollection** skapar en Power BI-arbetsyta för din Azure-prenumeration i angiven resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="0bc20-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="0bc20-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0bc20-107">EXAMPLES</span></span>

### <span data-ttu-id="0bc20-108">Exempel 1: skapa en samling med arbets ytor</span><span class="sxs-lookup"><span data-stu-id="0bc20-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="0bc20-109">Det här kommandot skapar en arbets yta med namnet WCN11 i den angivna resurs gruppen på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="0bc20-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="0bc20-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0bc20-110">PARAMETERS</span></span>

### <span data-ttu-id="0bc20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc20-111">-DefaultProfile</span></span>
<span data-ttu-id="0bc20-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0bc20-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bc20-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="0bc20-113">-Location</span></span>
<span data-ttu-id="0bc20-114">Anger den Azure-plats där den här cmdleten skapar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="0bc20-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc20-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc20-115">-ResourceGroupName</span></span>
<span data-ttu-id="0bc20-116">Anger namnet på den resurs grupp som den här cmdleten skapar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="0bc20-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="0bc20-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0bc20-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0bc20-118">Anger ett namn för Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="0bc20-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="0bc20-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0bc20-119">-Confirm</span></span>
<span data-ttu-id="0bc20-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0bc20-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bc20-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bc20-121">-WhatIf</span></span>
<span data-ttu-id="0bc20-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0bc20-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bc20-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0bc20-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bc20-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc20-124">CommonParameters</span></span>
<span data-ttu-id="0bc20-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bc20-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc20-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bc20-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc20-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0bc20-127">INPUTS</span></span>

### <span data-ttu-id="0bc20-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0bc20-128">System.String</span></span>

## <span data-ttu-id="0bc20-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0bc20-129">OUTPUTS</span></span>

### <span data-ttu-id="0bc20-130">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0bc20-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="0bc20-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0bc20-131">NOTES</span></span>

## <span data-ttu-id="0bc20-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0bc20-132">RELATED LINKS</span></span>

[<span data-ttu-id="0bc20-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0bc20-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="0bc20-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0bc20-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


