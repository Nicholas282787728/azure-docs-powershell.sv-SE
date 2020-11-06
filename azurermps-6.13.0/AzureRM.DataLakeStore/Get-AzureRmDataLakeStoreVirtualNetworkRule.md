---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1b404a42c3d40138408d7fb6f2c13a8af91c45c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575220"
---
# <span data-ttu-id="d248e-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d248e-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d248e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d248e-102">SYNOPSIS</span></span>
<span data-ttu-id="d248e-103">Hämtar de angivna virtuella nätverks reglerna i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d248e-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="d248e-104">Om ingen virtuell nätverks regel anges visas en lista med alla virtuella nätverks regler för kontot.</span><span class="sxs-lookup"><span data-stu-id="d248e-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d248e-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d248e-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d248e-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d248e-106">DESCRIPTION</span></span>
<span data-ttu-id="d248e-107">Den Get-AzureRmDataLakeStoreVirtualNetworkRule cmdleten hämtar de angivna virtuella nätverks reglerna i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d248e-107">The Get-AzureRmDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="d248e-108">Om ingen virtuell nätverks regel anges visas en lista med alla virtuella nätverks regler för kontot.</span><span class="sxs-lookup"><span data-stu-id="d248e-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="d248e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d248e-109">EXAMPLES</span></span>

### <span data-ttu-id="d248e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d248e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="d248e-111">Returnerar den virtuella nätverks regeln med namnet "myVNET" från kontot "DLS"</span><span class="sxs-lookup"><span data-stu-id="d248e-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="d248e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d248e-112">PARAMETERS</span></span>

### <span data-ttu-id="d248e-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="d248e-113">-Account</span></span>
<span data-ttu-id="d248e-114">Kontot för data Lake Store för att hämta regeln för virtuell nätverks trafik från</span><span class="sxs-lookup"><span data-stu-id="d248e-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="d248e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d248e-115">-DefaultProfile</span></span>
<span data-ttu-id="d248e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d248e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d248e-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d248e-117">-Name</span></span>
<span data-ttu-id="d248e-118">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="d248e-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="d248e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d248e-119">CommonParameters</span></span>
<span data-ttu-id="d248e-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d248e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d248e-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d248e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d248e-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d248e-122">INPUTS</span></span>

### <span data-ttu-id="d248e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d248e-123">System.String</span></span>

## <span data-ttu-id="d248e-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d248e-124">OUTPUTS</span></span>

### <span data-ttu-id="d248e-125">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d248e-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d248e-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d248e-126">NOTES</span></span>

## <span data-ttu-id="d248e-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d248e-127">RELATED LINKS</span></span>
