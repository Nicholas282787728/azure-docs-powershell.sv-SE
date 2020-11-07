---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926706"
---
# <span data-ttu-id="e823a-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e823a-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e823a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e823a-102">SYNOPSIS</span></span>
<span data-ttu-id="e823a-103">Hämtar de angivna virtuella nätverks reglerna i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e823a-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e823a-104">Om ingen virtuell nätverks regel anges visas en lista med alla virtuella nätverks regler för kontot.</span><span class="sxs-lookup"><span data-stu-id="e823a-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="e823a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e823a-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e823a-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e823a-106">DESCRIPTION</span></span>
<span data-ttu-id="e823a-107">Den Get-AzDataLakeStoreVirtualNetworkRule cmdleten hämtar de angivna virtuella nätverks reglerna i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e823a-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e823a-108">Om ingen virtuell nätverks regel anges visas en lista med alla virtuella nätverks regler för kontot.</span><span class="sxs-lookup"><span data-stu-id="e823a-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="e823a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e823a-109">EXAMPLES</span></span>

### <span data-ttu-id="e823a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e823a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="e823a-111">Returnerar den virtuella nätverks regeln med namnet "myVNET" från kontot "DLS"</span><span class="sxs-lookup"><span data-stu-id="e823a-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="e823a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e823a-112">PARAMETERS</span></span>

### <span data-ttu-id="e823a-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="e823a-113">-Account</span></span>
<span data-ttu-id="e823a-114">Kontot för data Lake Store för att hämta regeln för virtuell nätverks trafik från</span><span class="sxs-lookup"><span data-stu-id="e823a-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="e823a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e823a-115">-DefaultProfile</span></span>
<span data-ttu-id="e823a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e823a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e823a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e823a-117">-Name</span></span>
<span data-ttu-id="e823a-118">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="e823a-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e823a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e823a-119">CommonParameters</span></span>
<span data-ttu-id="e823a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e823a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e823a-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e823a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e823a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e823a-122">INPUTS</span></span>

### <span data-ttu-id="e823a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e823a-123">System.String</span></span>

## <span data-ttu-id="e823a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e823a-124">OUTPUTS</span></span>

### <span data-ttu-id="e823a-125">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e823a-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e823a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e823a-126">NOTES</span></span>

## <span data-ttu-id="e823a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e823a-127">RELATED LINKS</span></span>
