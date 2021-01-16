---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: a13125695ab5f4c57ab2e7013d64fff376643076
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397496"
---
# <span data-ttu-id="6e63d-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e63d-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="6e63d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e63d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e63d-103">Lägger till en brand Väggs regel till det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="6e63d-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="6e63d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e63d-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e63d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e63d-105">DESCRIPTION</span></span>
<span data-ttu-id="6e63d-106">Cmdleten **Add-AzDataLakeStoreFirewallRule** lägger till en brand Väggs regel i det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="6e63d-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="6e63d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e63d-107">EXAMPLES</span></span>

### <span data-ttu-id="6e63d-108">Exempel 1: lägga till en ny brand Väggs regel i ett data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="6e63d-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="6e63d-109">Detta skapar en ny brand Väggs regel som heter "min regel" i kontot "ContosoADL" med ett IP-intervall på 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="6e63d-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="6e63d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e63d-110">PARAMETERS</span></span>

### <span data-ttu-id="6e63d-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="6e63d-111">-Account</span></span>
<span data-ttu-id="6e63d-112">Data Lake Store-konto för att lägga till brand Väggs regeln i</span><span class="sxs-lookup"><span data-stu-id="6e63d-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="6e63d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e63d-113">-DefaultProfile</span></span>
<span data-ttu-id="6e63d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6e63d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e63d-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="6e63d-115">-EndIpAddress</span></span>
<span data-ttu-id="6e63d-116">Slutet på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="6e63d-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="6e63d-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="6e63d-117">-Name</span></span>
<span data-ttu-id="6e63d-118">Namnet på den brand Väggs regel som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="6e63d-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="6e63d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e63d-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e63d-120">Namnet på den resurs grupp under vilken kontot för att lägga till brand Väggs regeln är.</span><span class="sxs-lookup"><span data-stu-id="6e63d-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="6e63d-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="6e63d-121">-StartIpAddress</span></span>
<span data-ttu-id="6e63d-122">Början på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="6e63d-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="6e63d-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6e63d-123">-Confirm</span></span>
<span data-ttu-id="6e63d-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6e63d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e63d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e63d-125">-WhatIf</span></span>
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

### <span data-ttu-id="6e63d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e63d-126">CommonParameters</span></span>
<span data-ttu-id="6e63d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e63d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e63d-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e63d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e63d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e63d-129">INPUTS</span></span>

### <span data-ttu-id="6e63d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6e63d-130">System.String</span></span>

## <span data-ttu-id="6e63d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e63d-131">OUTPUTS</span></span>

### <span data-ttu-id="6e63d-132">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e63d-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="6e63d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e63d-133">NOTES</span></span>

## <span data-ttu-id="6e63d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e63d-134">RELATED LINKS</span></span>
