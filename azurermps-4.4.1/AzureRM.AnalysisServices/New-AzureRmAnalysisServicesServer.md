---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0093393f926af257e07b7d697a7f267fa62b483a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573788"
---
# <span data-ttu-id="7b6d4-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7b6d4-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="7b6d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b6d4-102">SYNOPSIS</span></span>
<span data-ttu-id="7b6d4-103">Skapar en ny Analysis Services-server</span><span class="sxs-lookup"><span data-stu-id="7b6d4-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b6d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b6d4-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b6d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b6d4-105">DESCRIPTION</span></span>
<span data-ttu-id="7b6d4-106">New-AzureRmAnalysisServicesServer-cmdleten skapar en ny Analysis Services-server</span><span class="sxs-lookup"><span data-stu-id="7b6d4-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="7b6d4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b6d4-107">EXAMPLES</span></span>

### <span data-ttu-id="7b6d4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7b6d4-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="7b6d4-109">Skapar en server med namnet testserver i Azure-regionen West-US och i resurs grupp testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="7b6d4-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="7b6d4-110">SKU-nivån för servern blir S1.</span><span class="sxs-lookup"><span data-stu-id="7b6d4-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="7b6d4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b6d4-111">PARAMETERS</span></span>

### <span data-ttu-id="7b6d4-112">-Administratör</span><span class="sxs-lookup"><span data-stu-id="7b6d4-112">-Administrator</span></span>
<span data-ttu-id="7b6d4-113">En sträng som representerar en kommaseparerad lista över användare eller grupper som ska anges som administratörer på servern.</span><span class="sxs-lookup"><span data-stu-id="7b6d4-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="7b6d4-114">Användare eller grupper måste ange UPN-format, t. ex. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7b6d4-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b6d4-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="7b6d4-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="7b6d4-116">URI för BLOB-behållare för säkerhets kopiering av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="7b6d4-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b6d4-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="7b6d4-117">-Location</span></span>
<span data-ttu-id="7b6d4-118">Azure-regionen där Analysis Services-servern finns</span><span class="sxs-lookup"><span data-stu-id="7b6d4-118">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b6d4-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="7b6d4-119">-Name</span></span>
<span data-ttu-id="7b6d4-120">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="7b6d4-120">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="7b6d4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b6d4-121">-ResourceGroupName</span></span>
<span data-ttu-id="7b6d4-122">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="7b6d4-122">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="7b6d4-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="7b6d4-123">-Sku</span></span>
<span data-ttu-id="7b6d4-124">Namnet på SKU för servern.</span><span class="sxs-lookup"><span data-stu-id="7b6d4-124">The name of the Sku for the server.</span></span>
<span data-ttu-id="7b6d4-125">De värden som stöds är 0 ', ' 1 ', är 2 ', är 4 ' för standard nivån; "B1", "B2" för bas nivån och "d" för utvecklings nivån.</span><span class="sxs-lookup"><span data-stu-id="7b6d4-125">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b6d4-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7b6d4-126">-Tag</span></span>
<span data-ttu-id="7b6d4-127">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="7b6d4-127">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b6d4-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7b6d4-128">-Confirm</span></span>
<span data-ttu-id="7b6d4-129">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="7b6d4-129">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b6d4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b6d4-130">-WhatIf</span></span>
<span data-ttu-id="7b6d4-131">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="7b6d4-131">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b6d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b6d4-132">CommonParameters</span></span>
<span data-ttu-id="7b6d4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b6d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b6d4-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b6d4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b6d4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b6d4-135">INPUTS</span></span>

## <span data-ttu-id="7b6d4-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b6d4-136">OUTPUTS</span></span>

### <span data-ttu-id="7b6d4-137">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7b6d4-137">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="7b6d4-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b6d4-138">NOTES</span></span>
<span data-ttu-id="7b6d4-139">Alias: New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="7b6d4-139">Alias: New-AzureAs</span></span>

## <span data-ttu-id="7b6d4-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b6d4-140">RELATED LINKS</span></span>

[<span data-ttu-id="7b6d4-141">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7b6d4-141">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="7b6d4-142">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7b6d4-142">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
