---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 45784bdcb684c1bd98ef1891042ad3ff6a172381
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756988"
---
# <span data-ttu-id="a5171-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a5171-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a5171-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5171-102">SYNOPSIS</span></span>
<span data-ttu-id="a5171-103">Lägger till en brand Väggs regel till det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="a5171-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5171-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5171-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5171-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5171-105">DESCRIPTION</span></span>
<span data-ttu-id="a5171-106">Cmdleten **Add-AzureRmDataLakeStoreFirewallRule** lägger till en brand Väggs regel i det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="a5171-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="a5171-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5171-107">EXAMPLES</span></span>

### <span data-ttu-id="a5171-108">Exempel 1: lägga till en ny brand Väggs regel i ett data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="a5171-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="a5171-109">Detta skapar en ny brand Väggs regel som heter "min regel" i kontot "ContosoADL" med ett IP-intervall på 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="a5171-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="a5171-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5171-110">PARAMETERS</span></span>

### <span data-ttu-id="a5171-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="a5171-111">-Account</span></span>
<span data-ttu-id="a5171-112">Data Lake Store-konto för att lägga till brand Väggs regeln i</span><span class="sxs-lookup"><span data-stu-id="a5171-112">The Data Lake Store account to add the firewall rule to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5171-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5171-113">-EndIpAddress</span></span>
<span data-ttu-id="a5171-114">Slutet på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="a5171-114">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5171-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5171-115">-Name</span></span>
<span data-ttu-id="a5171-116">Namnet på den brand Väggs regel som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="a5171-116">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="a5171-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5171-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5171-118">Namnet på den resurs grupp under vilken kontot för att lägga till brand Väggs regeln är.</span><span class="sxs-lookup"><span data-stu-id="a5171-118">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5171-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5171-119">-StartIpAddress</span></span>
<span data-ttu-id="a5171-120">Början på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="a5171-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="a5171-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5171-121">-Confirm</span></span>
<span data-ttu-id="a5171-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5171-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5171-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5171-123">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5171-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5171-124">-DefaultProfile</span></span>
<span data-ttu-id="a5171-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5171-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5171-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5171-126">CommonParameters</span></span>
<span data-ttu-id="a5171-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5171-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5171-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5171-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5171-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5171-129">INPUTS</span></span>

## <span data-ttu-id="a5171-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5171-130">OUTPUTS</span></span>

### <span data-ttu-id="a5171-131">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a5171-131">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="a5171-132">Brand Väggs regeln som har lagts till.</span><span class="sxs-lookup"><span data-stu-id="a5171-132">The firewall rule that was added.</span></span>

## <span data-ttu-id="a5171-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5171-133">NOTES</span></span>

## <span data-ttu-id="a5171-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5171-134">RELATED LINKS</span></span>

