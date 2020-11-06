---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: b7140570ecf6464483d0dc7da67e10f8b4ed5d70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573978"
---
# <span data-ttu-id="f452c-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f452c-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f452c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f452c-102">SYNOPSIS</span></span>
<span data-ttu-id="f452c-103">Uppdaterar en brand Väggs regel i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="f452c-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f452c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f452c-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f452c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f452c-105">DESCRIPTION</span></span>
<span data-ttu-id="f452c-106">Cmdleten **set-AzureRmDataLakeAnalyticsFirewallRule** uppdaterar en brand Väggs regel i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="f452c-106">The **Set-AzureRmDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f452c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f452c-107">EXAMPLES</span></span>

### <span data-ttu-id="f452c-108">Exempel 1: uppdatera en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="f452c-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="f452c-109">Det här kommandot uppdaterar brand Väggs regeln med namnet "brand Väggs regel" i kontot "ContosoAdlAcct" för att ha det nya IP-intervallet: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="f452c-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="f452c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f452c-110">PARAMETERS</span></span>

### <span data-ttu-id="f452c-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="f452c-111">-Account</span></span>
<span data-ttu-id="f452c-112">Data Lake Analytics-konto för att uppdatera brand Väggs regeln i</span><span class="sxs-lookup"><span data-stu-id="f452c-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="f452c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f452c-113">-DefaultProfile</span></span>
<span data-ttu-id="f452c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f452c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f452c-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="f452c-115">-EndIpAddress</span></span>
<span data-ttu-id="f452c-116">Slutet på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="f452c-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="f452c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f452c-117">-Name</span></span>
<span data-ttu-id="f452c-118">Namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="f452c-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="f452c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f452c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f452c-120">Namnet på den resurs grupp som du vill hämta kontot för.</span><span class="sxs-lookup"><span data-stu-id="f452c-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="f452c-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="f452c-121">-StartIpAddress</span></span>
<span data-ttu-id="f452c-122">Början på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="f452c-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="f452c-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f452c-123">-Confirm</span></span>
<span data-ttu-id="f452c-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f452c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f452c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f452c-125">-WhatIf</span></span>
<span data-ttu-id="f452c-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f452c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f452c-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f452c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f452c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f452c-128">CommonParameters</span></span>
<span data-ttu-id="f452c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f452c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f452c-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f452c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f452c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f452c-131">INPUTS</span></span>

### <span data-ttu-id="f452c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f452c-132">System.String</span></span>

## <span data-ttu-id="f452c-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f452c-133">OUTPUTS</span></span>

### <span data-ttu-id="f452c-134">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f452c-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f452c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f452c-135">NOTES</span></span>

## <span data-ttu-id="f452c-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f452c-136">RELATED LINKS</span></span>
