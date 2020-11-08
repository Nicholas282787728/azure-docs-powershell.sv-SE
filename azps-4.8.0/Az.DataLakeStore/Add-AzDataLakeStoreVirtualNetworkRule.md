---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261891"
---
# <span data-ttu-id="72348-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="72348-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="72348-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72348-102">SYNOPSIS</span></span>
<span data-ttu-id="72348-103">Lägger till en virtuell nätverks regel till det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="72348-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="72348-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72348-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72348-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72348-105">DESCRIPTION</span></span>
<span data-ttu-id="72348-106">Cmdleten **Add-AzDataLakeStoreVirtualNetworkRule** lägger till en virtuell nätverks regel till det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="72348-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="72348-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72348-107">EXAMPLES</span></span>

### <span data-ttu-id="72348-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="72348-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="72348-109">Detta skapar en ny virtuell nätverks regel med namnet "myVNET" i kontot "DLS" med ett Subnet ID "testId"</span><span class="sxs-lookup"><span data-stu-id="72348-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="72348-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72348-110">PARAMETERS</span></span>

### <span data-ttu-id="72348-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="72348-111">-Account</span></span>
<span data-ttu-id="72348-112">Data Lake Store-konto för att lägga till regeln för virtuella nätverk i</span><span class="sxs-lookup"><span data-stu-id="72348-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="72348-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72348-113">-DefaultProfile</span></span>
<span data-ttu-id="72348-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72348-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72348-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="72348-115">-Name</span></span>
<span data-ttu-id="72348-116">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="72348-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="72348-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="72348-117">-SubnetId</span></span>
<span data-ttu-id="72348-118">SubnetId för den virtuella nätverks regeln</span><span class="sxs-lookup"><span data-stu-id="72348-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="72348-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72348-119">-Confirm</span></span>
<span data-ttu-id="72348-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72348-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72348-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72348-121">-WhatIf</span></span>
<span data-ttu-id="72348-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72348-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72348-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72348-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72348-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72348-124">CommonParameters</span></span>
<span data-ttu-id="72348-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72348-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72348-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72348-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72348-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72348-127">INPUTS</span></span>

### <span data-ttu-id="72348-128">System. String</span><span class="sxs-lookup"><span data-stu-id="72348-128">System.String</span></span>

## <span data-ttu-id="72348-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72348-129">OUTPUTS</span></span>

### <span data-ttu-id="72348-130">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="72348-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="72348-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72348-131">NOTES</span></span>

## <span data-ttu-id="72348-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72348-132">RELATED LINKS</span></span>
