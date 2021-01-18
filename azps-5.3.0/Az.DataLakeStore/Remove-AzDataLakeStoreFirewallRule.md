---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e583379f9541c056943081b804a84ecd7bee7bf5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520108"
---
# <span data-ttu-id="ab557-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ab557-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="ab557-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab557-102">SYNOPSIS</span></span>
<span data-ttu-id="ab557-103">Tar bort den angivna brand Väggs regeln i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab557-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="ab557-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab557-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab557-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab557-105">DESCRIPTION</span></span>
<span data-ttu-id="ab557-106">Cmdleten **Remove-AzDataLakeStoreFirewallRule** tar bort den angivna brand Väggs regeln i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab557-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="ab557-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab557-107">EXAMPLES</span></span>

### <span data-ttu-id="ab557-108">Exempel 1: ta bort en brand Väggs regel från ett konto</span><span class="sxs-lookup"><span data-stu-id="ab557-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="ab557-109">Tar bort brand Väggs regeln "MyFirewallRule" från kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="ab557-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="ab557-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab557-110">PARAMETERS</span></span>

### <span data-ttu-id="ab557-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="ab557-111">-Account</span></span>
<span data-ttu-id="ab557-112">Data Lake Store-konto för att uppdatera brand Väggs regeln i</span><span class="sxs-lookup"><span data-stu-id="ab557-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="ab557-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab557-113">-DefaultProfile</span></span>
<span data-ttu-id="ab557-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ab557-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab557-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab557-115">-Name</span></span>
<span data-ttu-id="ab557-116">Namnet på den brand Väggs regel som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ab557-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="ab557-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab557-117">-PassThru</span></span>
<span data-ttu-id="ab557-118">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ab557-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="ab557-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab557-119">-ResourceGroupName</span></span>
<span data-ttu-id="ab557-120">Anger namnet på den resurs grupp som innehåller kontot som brand Väggs regeln ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="ab557-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="ab557-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab557-121">-Confirm</span></span>
<span data-ttu-id="ab557-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab557-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab557-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab557-123">-WhatIf</span></span>
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

### <span data-ttu-id="ab557-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab557-124">CommonParameters</span></span>
<span data-ttu-id="ab557-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab557-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab557-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab557-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab557-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab557-127">INPUTS</span></span>

### <span data-ttu-id="ab557-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ab557-128">System.String</span></span>

### <span data-ttu-id="ab557-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ab557-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ab557-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab557-130">OUTPUTS</span></span>

### <span data-ttu-id="ab557-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab557-131">System.Boolean</span></span>

## <span data-ttu-id="ab557-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab557-132">NOTES</span></span>

## <span data-ttu-id="ab557-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab557-133">RELATED LINKS</span></span>
