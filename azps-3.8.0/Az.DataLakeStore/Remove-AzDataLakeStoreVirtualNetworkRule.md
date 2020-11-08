---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 9e455b7160b731f20e5dad6230b2015f73ca5390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092766"
---
# <span data-ttu-id="445cb-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="445cb-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="445cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="445cb-102">SYNOPSIS</span></span>
<span data-ttu-id="445cb-103">Tar bort den angivna regeln för virtuella nätverk i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="445cb-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="445cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="445cb-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="445cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="445cb-105">DESCRIPTION</span></span>
<span data-ttu-id="445cb-106">Cmdleten **Remove-AzDataLakeStoreVirtualNetworkRule** tar bort den angivna regeln för virtuella nätverk i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="445cb-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="445cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="445cb-107">EXAMPLES</span></span>

### <span data-ttu-id="445cb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="445cb-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="445cb-109">Tar bort den virtuella nätverks regeln "myVNET" från kontot "DLS"</span><span class="sxs-lookup"><span data-stu-id="445cb-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="445cb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="445cb-110">PARAMETERS</span></span>

### <span data-ttu-id="445cb-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="445cb-111">-Account</span></span>
<span data-ttu-id="445cb-112">Kontot för data Lake Store för att uppdatera regeln för virtuella nätverk i</span><span class="sxs-lookup"><span data-stu-id="445cb-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="445cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="445cb-113">-DefaultProfile</span></span>
<span data-ttu-id="445cb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="445cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="445cb-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="445cb-115">-Name</span></span>
<span data-ttu-id="445cb-116">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="445cb-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="445cb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="445cb-117">-PassThru</span></span>
<span data-ttu-id="445cb-118">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="445cb-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="445cb-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="445cb-119">-Confirm</span></span>
<span data-ttu-id="445cb-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="445cb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="445cb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="445cb-121">-WhatIf</span></span>
<span data-ttu-id="445cb-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="445cb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="445cb-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="445cb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="445cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445cb-124">CommonParameters</span></span>
<span data-ttu-id="445cb-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="445cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445cb-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="445cb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445cb-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="445cb-127">INPUTS</span></span>

### <span data-ttu-id="445cb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="445cb-128">System.String</span></span>

## <span data-ttu-id="445cb-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="445cb-129">OUTPUTS</span></span>

### <span data-ttu-id="445cb-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="445cb-130">System.Boolean</span></span>

## <span data-ttu-id="445cb-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="445cb-131">NOTES</span></span>

## <span data-ttu-id="445cb-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="445cb-132">RELATED LINKS</span></span>
