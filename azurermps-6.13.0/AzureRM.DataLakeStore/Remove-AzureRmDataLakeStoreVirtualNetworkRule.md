---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 196d0eba5119ab984f9ffc632a301d3e65157f63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756186"
---
# <span data-ttu-id="9a6fb-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9a6fb-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="9a6fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a6fb-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6fb-103">Tar bort den angivna regeln för virtuella nätverk i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9a6fb-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a6fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a6fb-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a6fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a6fb-105">DESCRIPTION</span></span>
<span data-ttu-id="9a6fb-106">Cmdleten **Remove-AzureRmDataLakeStoreVirtualNetworkRule** tar bort den angivna regeln för virtuella nätverk i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9a6fb-106">The **Remove-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="9a6fb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a6fb-107">EXAMPLES</span></span>

### <span data-ttu-id="9a6fb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9a6fb-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="9a6fb-109">Tar bort den virtuella nätverks regeln "myVNET" från kontot "DLS"</span><span class="sxs-lookup"><span data-stu-id="9a6fb-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="9a6fb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a6fb-110">PARAMETERS</span></span>

### <span data-ttu-id="9a6fb-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="9a6fb-111">-Account</span></span>
<span data-ttu-id="9a6fb-112">Kontot för data Lake Store för att uppdatera regeln för virtuella nätverk i</span><span class="sxs-lookup"><span data-stu-id="9a6fb-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="9a6fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6fb-113">-DefaultProfile</span></span>
<span data-ttu-id="9a6fb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a6fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a6fb-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a6fb-115">-Name</span></span>
<span data-ttu-id="9a6fb-116">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="9a6fb-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6fb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a6fb-117">-PassThru</span></span>
<span data-ttu-id="9a6fb-118">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="9a6fb-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6fb-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9a6fb-119">-Confirm</span></span>
<span data-ttu-id="9a6fb-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9a6fb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a6fb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a6fb-121">-WhatIf</span></span>
<span data-ttu-id="9a6fb-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9a6fb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a6fb-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9a6fb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a6fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6fb-124">CommonParameters</span></span>
<span data-ttu-id="9a6fb-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a6fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6fb-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a6fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6fb-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a6fb-127">INPUTS</span></span>

### <span data-ttu-id="9a6fb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9a6fb-128">System.String</span></span>

### <span data-ttu-id="9a6fb-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9a6fb-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9a6fb-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a6fb-130">OUTPUTS</span></span>

### <span data-ttu-id="9a6fb-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a6fb-131">System.Boolean</span></span>

## <span data-ttu-id="9a6fb-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a6fb-132">NOTES</span></span>

## <span data-ttu-id="9a6fb-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a6fb-133">RELATED LINKS</span></span>
