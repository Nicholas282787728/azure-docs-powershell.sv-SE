---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 9d0b360e7284086b1cfadcba6ad17c47c22b6cb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574294"
---
# <span data-ttu-id="026d1-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="026d1-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="026d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="026d1-102">SYNOPSIS</span></span>
<span data-ttu-id="026d1-103">Tar bort den angivna brand Väggs regeln i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="026d1-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="026d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="026d1-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="026d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="026d1-105">DESCRIPTION</span></span>
<span data-ttu-id="026d1-106">Cmdleten **Remove-AzureRmDataLakeStoreFirewallRule** tar bort den angivna brand Väggs regeln i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="026d1-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="026d1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="026d1-107">EXAMPLES</span></span>

### <span data-ttu-id="026d1-108">Exempel 1: ta bort en brand Väggs regel från ett konto</span><span class="sxs-lookup"><span data-stu-id="026d1-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="026d1-109">Tar bort brand Väggs regeln "MyFirewallRule" från kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="026d1-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="026d1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="026d1-110">PARAMETERS</span></span>

### <span data-ttu-id="026d1-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="026d1-111">-Account</span></span>
<span data-ttu-id="026d1-112">Data Lake Store-konto för att uppdatera brand Väggs regeln i</span><span class="sxs-lookup"><span data-stu-id="026d1-112">The Data Lake Store account to update the firewall rule in</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="026d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="026d1-113">-DefaultProfile</span></span>
<span data-ttu-id="026d1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="026d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="026d1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="026d1-115">-Name</span></span>
<span data-ttu-id="026d1-116">Namnet på den brand Väggs regel som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="026d1-116">The name of the firewall rule to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="026d1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="026d1-117">-PassThru</span></span>
<span data-ttu-id="026d1-118">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="026d1-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="026d1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="026d1-119">-ResourceGroupName</span></span>
<span data-ttu-id="026d1-120">Anger namnet på den resurs grupp som innehåller kontot som brand Väggs regeln ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="026d1-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="026d1-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="026d1-121">-Confirm</span></span>
<span data-ttu-id="026d1-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="026d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="026d1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="026d1-123">-WhatIf</span></span>
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

### <span data-ttu-id="026d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="026d1-124">CommonParameters</span></span>
<span data-ttu-id="026d1-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="026d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="026d1-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="026d1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="026d1-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="026d1-127">INPUTS</span></span>

### <span data-ttu-id="026d1-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="026d1-128">None</span></span>
<span data-ttu-id="026d1-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="026d1-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="026d1-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="026d1-130">OUTPUTS</span></span>

### <span data-ttu-id="026d1-131">bool</span><span class="sxs-lookup"><span data-stu-id="026d1-131">bool</span></span>
<span data-ttu-id="026d1-132">Om PassThru är angivet returneras sant när du är klar.</span><span class="sxs-lookup"><span data-stu-id="026d1-132">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="026d1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="026d1-133">NOTES</span></span>

## <span data-ttu-id="026d1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="026d1-134">RELATED LINKS</span></span>

