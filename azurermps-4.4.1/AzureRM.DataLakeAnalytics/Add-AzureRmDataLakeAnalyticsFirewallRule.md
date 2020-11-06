---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 585e0cd6a3cd74c8077833f6b5599b076c2a5db6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574700"
---
# <span data-ttu-id="fc4af-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fc4af-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="fc4af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc4af-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4af-103">Lägger till en brand Väggs regel i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="fc4af-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc4af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc4af-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc4af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc4af-105">DESCRIPTION</span></span>
<span data-ttu-id="fc4af-106">Cmdleten **Add-AzureRmDataLakeAnalyticsFirewallRule** lägger till en brand Väggs regel i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="fc4af-106">The **Add-AzureRmDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="fc4af-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc4af-107">EXAMPLES</span></span>

### <span data-ttu-id="fc4af-108">Exempel 1: lägga till en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="fc4af-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="fc4af-109">Det här kommandot lägger till brand Väggs regeln med namnet "brand Väggs regel" från kontot "ContosoAdlAcct" med IP-intervallet: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="fc4af-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="fc4af-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc4af-110">PARAMETERS</span></span>

### <span data-ttu-id="fc4af-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="fc4af-111">-Account</span></span>
<span data-ttu-id="fc4af-112">Data Lake Analytics-konto för att lägga till brand Väggs regeln i</span><span class="sxs-lookup"><span data-stu-id="fc4af-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="fc4af-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="fc4af-113">-EndIpAddress</span></span>
<span data-ttu-id="fc4af-114">Slutet på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="fc4af-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="fc4af-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc4af-115">-Name</span></span>
<span data-ttu-id="fc4af-116">Namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="fc4af-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="fc4af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc4af-117">-ResourceGroupName</span></span>
<span data-ttu-id="fc4af-118">Namnet på den resurs grupp som du vill hämta kontot för.</span><span class="sxs-lookup"><span data-stu-id="fc4af-118">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4af-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="fc4af-119">-StartIpAddress</span></span>
<span data-ttu-id="fc4af-120">Början på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="fc4af-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="fc4af-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fc4af-121">-Confirm</span></span>
<span data-ttu-id="fc4af-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fc4af-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc4af-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc4af-123">-WhatIf</span></span>
<span data-ttu-id="fc4af-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fc4af-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc4af-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fc4af-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc4af-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4af-126">-DefaultProfile</span></span>
<span data-ttu-id="fc4af-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc4af-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc4af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4af-128">CommonParameters</span></span>
<span data-ttu-id="fc4af-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4af-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc4af-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4af-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc4af-131">INPUTS</span></span>

### <span data-ttu-id="fc4af-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fc4af-132">System.String</span></span>

## <span data-ttu-id="fc4af-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc4af-133">OUTPUTS</span></span>

### <span data-ttu-id="fc4af-134">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fc4af-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="fc4af-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc4af-135">NOTES</span></span>

## <span data-ttu-id="fc4af-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc4af-136">RELATED LINKS</span></span>

