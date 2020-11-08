---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272986"
---
# <span data-ttu-id="39104-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="39104-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="39104-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39104-102">SYNOPSIS</span></span>
<span data-ttu-id="39104-103">Hämta egenskapen NetWorkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="39104-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="39104-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39104-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39104-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39104-105">DESCRIPTION</span></span>
<span data-ttu-id="39104-106">Cmdleten **Get-AzStorageAccountNetworkRuleSet** hämtar egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="39104-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="39104-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39104-107">EXAMPLES</span></span>

### <span data-ttu-id="39104-108">Exempel 1: get NetworkRule-egenskapen för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="39104-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="39104-109">Det här kommandot får egenskapen NetworkRule för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="39104-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="39104-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39104-110">PARAMETERS</span></span>

### <span data-ttu-id="39104-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39104-111">-DefaultProfile</span></span>
<span data-ttu-id="39104-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39104-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39104-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="39104-113">-Name</span></span>
<span data-ttu-id="39104-114">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="39104-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="39104-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39104-115">-ResourceGroupName</span></span>
<span data-ttu-id="39104-116">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="39104-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="39104-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39104-117">CommonParameters</span></span>
<span data-ttu-id="39104-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39104-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39104-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39104-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39104-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39104-120">INPUTS</span></span>

### <span data-ttu-id="39104-121">System. String</span><span class="sxs-lookup"><span data-stu-id="39104-121">System.String</span></span>

## <span data-ttu-id="39104-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39104-122">OUTPUTS</span></span>

### <span data-ttu-id="39104-123">Microsoft. Azure. commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="39104-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="39104-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39104-124">NOTES</span></span>

## <span data-ttu-id="39104-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39104-125">RELATED LINKS</span></span>
