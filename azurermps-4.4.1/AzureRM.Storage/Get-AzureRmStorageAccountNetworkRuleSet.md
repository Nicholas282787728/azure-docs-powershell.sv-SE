---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 00447be14fe61b76a4dbb4f62e3393bb76c1ddb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758259"
---
# <span data-ttu-id="cc3f5-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cc3f5-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="cc3f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="cc3f5-103">Hämta egenskapen NetWorkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="cc3f5-103">Get the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc3f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc3f5-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc3f5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc3f5-105">DESCRIPTION</span></span>
<span data-ttu-id="cc3f5-106">Cmdleten **Get-AzureRmStorageAccountNetworkRuleSet** hämtar egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="cc3f5-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="cc3f5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc3f5-107">EXAMPLES</span></span>

### <span data-ttu-id="cc3f5-108">Exempel 1: get NetworkRule-egenskapen för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="cc3f5-108">Example 1: Get NetworkRule property of a specified storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="cc3f5-109">Det här kommandot får egenskapen NetworkRule för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="cc3f5-109">This command gets NetworkRule property of a specified storage account</span></span>

## <span data-ttu-id="cc3f5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc3f5-110">PARAMETERS</span></span>

### <span data-ttu-id="cc3f5-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc3f5-111">-Name</span></span>
<span data-ttu-id="cc3f5-112">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="cc3f5-112">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="cc3f5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc3f5-113">-ResourceGroupName</span></span>
<span data-ttu-id="cc3f5-114">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="cc3f5-114">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="cc3f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc3f5-115">-DefaultProfile</span></span>
<span data-ttu-id="cc3f5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc3f5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc3f5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc3f5-117">CommonParameters</span></span>
<span data-ttu-id="cc3f5-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc3f5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc3f5-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc3f5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc3f5-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc3f5-120">INPUTS</span></span>

### <span data-ttu-id="cc3f5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="cc3f5-121">System.String</span></span>

## <span data-ttu-id="cc3f5-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc3f5-122">OUTPUTS</span></span>

### <span data-ttu-id="cc3f5-123">Microsoft. Azure. commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cc3f5-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="cc3f5-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc3f5-124">NOTES</span></span>

## <span data-ttu-id="cc3f5-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc3f5-125">RELATED LINKS</span></span>
