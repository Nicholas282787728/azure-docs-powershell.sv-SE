---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088972"
---
# <span data-ttu-id="b6b6f-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b6f-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="b6b6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b6f-103">Hämta egenskapen NetWorkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="b6b6f-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="b6b6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6b6f-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6b6f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6b6f-105">DESCRIPTION</span></span>
<span data-ttu-id="b6b6f-106">Cmdleten **Get-AzStorageAccountNetworkRuleSet** hämtar egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="b6b6f-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="b6b6f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6b6f-107">EXAMPLES</span></span>

### <span data-ttu-id="b6b6f-108">Exempel 1: get NetworkRule-egenskapen för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="b6b6f-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="b6b6f-109">Det här kommandot får egenskapen NetworkRule för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="b6b6f-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="b6b6f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6b6f-110">PARAMETERS</span></span>

### <span data-ttu-id="b6b6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b6f-111">-DefaultProfile</span></span>
<span data-ttu-id="b6b6f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b6f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6b6f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="b6b6f-113">-Name</span></span>
<span data-ttu-id="b6b6f-114">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="b6b6f-114">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b6f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6b6f-115">-ResourceGroupName</span></span>
<span data-ttu-id="b6b6f-116">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="b6b6f-116">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b6f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b6f-117">CommonParameters</span></span>
<span data-ttu-id="b6b6f-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b6f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b6f-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6b6f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b6f-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6b6f-120">INPUTS</span></span>

### <span data-ttu-id="b6b6f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b6b6f-121">System.String</span></span>

## <span data-ttu-id="b6b6f-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6b6f-122">OUTPUTS</span></span>

### <span data-ttu-id="b6b6f-123">Microsoft. Azure. commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6b6f-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="b6b6f-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6b6f-124">NOTES</span></span>

## <span data-ttu-id="b6b6f-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6b6f-125">RELATED LINKS</span></span>
