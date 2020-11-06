---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 981daec060f47a88b31454cd8d13711091bedcf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584608"
---
# <span data-ttu-id="a174a-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a174a-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="a174a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a174a-102">SYNOPSIS</span></span>
<span data-ttu-id="a174a-103">Skapar en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="a174a-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a174a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a174a-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a174a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a174a-105">DESCRIPTION</span></span>
<span data-ttu-id="a174a-106">Cmdleten **New-AzureRmPowerBIWorkspaceCollection** skapar en Power BI-arbetsyta för din Azure-prenumeration i angiven resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="a174a-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="a174a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a174a-107">EXAMPLES</span></span>

### <span data-ttu-id="a174a-108">Exempel 1: skapa en samling med arbets ytor</span><span class="sxs-lookup"><span data-stu-id="a174a-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="a174a-109">Det här kommandot skapar en arbets yta med namnet WCN11 i den angivna resurs gruppen på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="a174a-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="a174a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a174a-110">PARAMETERS</span></span>

### <span data-ttu-id="a174a-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="a174a-111">-Location</span></span>
<span data-ttu-id="a174a-112">Anger den Azure-plats där den här cmdleten skapar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="a174a-112">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="a174a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a174a-113">-ResourceGroupName</span></span>
<span data-ttu-id="a174a-114">Anger namnet på den resurs grupp som den här cmdleten skapar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="a174a-114">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="a174a-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="a174a-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="a174a-116">Anger ett namn för Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="a174a-116">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="a174a-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a174a-117">-Confirm</span></span>
<span data-ttu-id="a174a-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a174a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a174a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a174a-119">-WhatIf</span></span>
<span data-ttu-id="a174a-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a174a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a174a-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a174a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a174a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a174a-122">-DefaultProfile</span></span>
<span data-ttu-id="a174a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a174a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a174a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a174a-124">CommonParameters</span></span>
<span data-ttu-id="a174a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a174a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a174a-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a174a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a174a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a174a-127">INPUTS</span></span>

## <span data-ttu-id="a174a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a174a-128">OUTPUTS</span></span>

### <span data-ttu-id="a174a-129">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a174a-129">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="a174a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a174a-130">NOTES</span></span>

## <span data-ttu-id="a174a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a174a-131">RELATED LINKS</span></span>

[<span data-ttu-id="a174a-132">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a174a-132">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="a174a-133">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a174a-133">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


