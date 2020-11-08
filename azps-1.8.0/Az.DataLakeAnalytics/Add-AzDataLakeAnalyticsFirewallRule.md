---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: ecb6088b3ca257967faff49b47a7ec2f3c2bf7bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916994"
---
# <span data-ttu-id="2f897-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2f897-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="2f897-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f897-102">SYNOPSIS</span></span>
<span data-ttu-id="2f897-103">Lägger till en brand Väggs regel i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="2f897-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="2f897-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f897-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f897-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f897-105">DESCRIPTION</span></span>
<span data-ttu-id="2f897-106">Cmdleten **Add-AzDataLakeAnalyticsFirewallRule** lägger till en brand Väggs regel i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="2f897-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2f897-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f897-107">EXAMPLES</span></span>

### <span data-ttu-id="2f897-108">Exempel 1: lägga till en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="2f897-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="2f897-109">Det här kommandot lägger till brand Väggs regeln med namnet "brand Väggs regel" från kontot "ContosoAdlAcct" med IP-intervallet: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="2f897-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="2f897-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f897-110">PARAMETERS</span></span>

### <span data-ttu-id="2f897-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="2f897-111">-Account</span></span>
<span data-ttu-id="2f897-112">Data Lake Analytics-konto för att lägga till brand Väggs regeln i</span><span class="sxs-lookup"><span data-stu-id="2f897-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="2f897-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f897-113">-DefaultProfile</span></span>
<span data-ttu-id="2f897-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2f897-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f897-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="2f897-115">-EndIpAddress</span></span>
<span data-ttu-id="2f897-116">Slutet på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="2f897-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="2f897-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f897-117">-Name</span></span>
<span data-ttu-id="2f897-118">Namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="2f897-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="2f897-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f897-119">-ResourceGroupName</span></span>
<span data-ttu-id="2f897-120">Namnet på den resurs grupp som du vill hämta kontot för.</span><span class="sxs-lookup"><span data-stu-id="2f897-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="2f897-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="2f897-121">-StartIpAddress</span></span>
<span data-ttu-id="2f897-122">Början på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="2f897-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="2f897-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f897-123">-Confirm</span></span>
<span data-ttu-id="2f897-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f897-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f897-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f897-125">-WhatIf</span></span>
<span data-ttu-id="2f897-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f897-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f897-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f897-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f897-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f897-128">CommonParameters</span></span>
<span data-ttu-id="2f897-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f897-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f897-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f897-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f897-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f897-131">INPUTS</span></span>

### <span data-ttu-id="2f897-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2f897-132">System.String</span></span>

## <span data-ttu-id="2f897-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f897-133">OUTPUTS</span></span>

### <span data-ttu-id="2f897-134">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2f897-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="2f897-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f897-135">NOTES</span></span>

## <span data-ttu-id="2f897-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f897-136">RELATED LINKS</span></span>