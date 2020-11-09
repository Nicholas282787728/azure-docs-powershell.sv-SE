---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 879897b6d89e5a1e34ee9f61714628aa741a670f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320683"
---
# <span data-ttu-id="b0d13-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b0d13-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="b0d13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0d13-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d13-103">Tar bort en brand Väggs regel från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="b0d13-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="b0d13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0d13-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0d13-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0d13-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d13-106">Cmdleten **Remove-AzDataLakeAnalyticsFirewallRule** tar bort en brand Väggs regel från ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="b0d13-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="b0d13-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0d13-107">EXAMPLES</span></span>

### <span data-ttu-id="b0d13-108">Exempel 1: ta bort en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="b0d13-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="b0d13-109">Det här kommandot tar bort brand Väggs regeln med namnet "brand Väggs regel" från kontot "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="b0d13-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="b0d13-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0d13-110">PARAMETERS</span></span>

### <span data-ttu-id="b0d13-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="b0d13-111">-Account</span></span>
<span data-ttu-id="b0d13-112">Data Lake Analytics-kontot som tar bort brand Väggs regeln från</span><span class="sxs-lookup"><span data-stu-id="b0d13-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="b0d13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d13-113">-DefaultProfile</span></span>
<span data-ttu-id="b0d13-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b0d13-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0d13-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0d13-115">-Name</span></span>
<span data-ttu-id="b0d13-116">Namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="b0d13-116">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d13-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0d13-117">-PassThru</span></span>
<span data-ttu-id="b0d13-118">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b0d13-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d13-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d13-119">-ResourceGroupName</span></span>
<span data-ttu-id="b0d13-120">Namnet på den resurs grupp som du vill hämta kontot för.</span><span class="sxs-lookup"><span data-stu-id="b0d13-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="b0d13-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b0d13-121">-Confirm</span></span>
<span data-ttu-id="b0d13-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b0d13-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0d13-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0d13-123">-WhatIf</span></span>
<span data-ttu-id="b0d13-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b0d13-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0d13-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b0d13-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0d13-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d13-126">CommonParameters</span></span>
<span data-ttu-id="b0d13-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d13-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d13-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0d13-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d13-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0d13-129">INPUTS</span></span>

### <span data-ttu-id="b0d13-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b0d13-130">System.String</span></span>

### <span data-ttu-id="b0d13-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b0d13-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b0d13-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0d13-132">OUTPUTS</span></span>

### <span data-ttu-id="b0d13-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0d13-133">System.Boolean</span></span>

## <span data-ttu-id="b0d13-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0d13-134">NOTES</span></span>

## <span data-ttu-id="b0d13-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0d13-135">RELATED LINKS</span></span>
