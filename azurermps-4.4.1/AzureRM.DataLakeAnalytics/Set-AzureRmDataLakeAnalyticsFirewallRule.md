---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 6f19df2f234bd66ac629f8238aa2cfea257106df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756990"
---
# <span data-ttu-id="7be31-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7be31-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="7be31-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7be31-102">SYNOPSIS</span></span>
<span data-ttu-id="7be31-103">Uppdaterar en brand Väggs regel i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="7be31-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7be31-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7be31-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7be31-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7be31-105">DESCRIPTION</span></span>
<span data-ttu-id="7be31-106">Cmdleten **set-AzureRmDataLakeAnalyticsFirewallRule** uppdaterar en brand Väggs regel i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="7be31-106">The **Set-AzureRmDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7be31-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7be31-107">EXAMPLES</span></span>

### <span data-ttu-id="7be31-108">Exempel 1: uppdatera en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="7be31-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="7be31-109">Det här kommandot uppdaterar brand Väggs regeln med namnet "brand Väggs regel" i kontot "ContosoAdlAcct" för att ha det nya IP-intervallet: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="7be31-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="7be31-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7be31-110">PARAMETERS</span></span>

### <span data-ttu-id="7be31-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="7be31-111">-Account</span></span>
<span data-ttu-id="7be31-112">Data Lake Analytics-konto för att uppdatera brand Väggs regeln i</span><span class="sxs-lookup"><span data-stu-id="7be31-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="7be31-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="7be31-113">-EndIpAddress</span></span>
<span data-ttu-id="7be31-114">Slutet på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="7be31-114">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be31-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="7be31-115">-Name</span></span>
<span data-ttu-id="7be31-116">Namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="7be31-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="7be31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be31-117">-ResourceGroupName</span></span>
<span data-ttu-id="7be31-118">Namnet på den resurs grupp som du vill hämta kontot för.</span><span class="sxs-lookup"><span data-stu-id="7be31-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="7be31-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="7be31-119">-StartIpAddress</span></span>
<span data-ttu-id="7be31-120">Början på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="7be31-120">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be31-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7be31-121">-Confirm</span></span>
<span data-ttu-id="7be31-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7be31-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7be31-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7be31-123">-WhatIf</span></span>
<span data-ttu-id="7be31-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7be31-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7be31-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7be31-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7be31-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be31-126">-DefaultProfile</span></span>
<span data-ttu-id="7be31-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7be31-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7be31-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be31-128">CommonParameters</span></span>
<span data-ttu-id="7be31-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7be31-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be31-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7be31-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be31-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7be31-131">INPUTS</span></span>

### <span data-ttu-id="7be31-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7be31-132">System.String</span></span>

## <span data-ttu-id="7be31-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7be31-133">OUTPUTS</span></span>

### <span data-ttu-id="7be31-134">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7be31-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="7be31-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7be31-135">NOTES</span></span>

## <span data-ttu-id="7be31-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7be31-136">RELATED LINKS</span></span>

