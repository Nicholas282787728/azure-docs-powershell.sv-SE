---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 0a316ee8e4d1d7c8d58e2444aa6cdfadbc5e0367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576727"
---
# <span data-ttu-id="d922c-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d922c-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d922c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d922c-102">SYNOPSIS</span></span>
<span data-ttu-id="d922c-103">Hämta egenskapen NetWorkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="d922c-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d922c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d922c-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d922c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d922c-105">DESCRIPTION</span></span>
<span data-ttu-id="d922c-106">Cmdleten **Get-AzureRmStorageAccountNetworkRuleSet** hämtar egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="d922c-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="d922c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d922c-107">EXAMPLES</span></span>

### <span data-ttu-id="d922c-108">Exempel 1: get NetworkRule-egenskapen för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="d922c-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="d922c-109">Det här kommandot får egenskapen NetworkRule för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="d922c-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="d922c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d922c-110">PARAMETERS</span></span>

### <span data-ttu-id="d922c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d922c-111">-DefaultProfile</span></span>
<span data-ttu-id="d922c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d922c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d922c-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d922c-113">-Name</span></span>
<span data-ttu-id="d922c-114">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="d922c-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="d922c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d922c-115">-ResourceGroupName</span></span>
<span data-ttu-id="d922c-116">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="d922c-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d922c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d922c-117">CommonParameters</span></span>
<span data-ttu-id="d922c-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d922c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d922c-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d922c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d922c-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d922c-120">INPUTS</span></span>

### <span data-ttu-id="d922c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d922c-121">System.String</span></span>

## <span data-ttu-id="d922c-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d922c-122">OUTPUTS</span></span>

### <span data-ttu-id="d922c-123">Microsoft. Azure. commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d922c-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d922c-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d922c-124">NOTES</span></span>

## <span data-ttu-id="d922c-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d922c-125">RELATED LINKS</span></span>
