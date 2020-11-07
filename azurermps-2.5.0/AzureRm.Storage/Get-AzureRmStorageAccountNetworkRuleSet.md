---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
ms.openlocfilehash: 8e3aa3bd313947712ef3831b83c75bb1349adb4f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929570"
---
# <span data-ttu-id="0a7a3-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a7a3-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="0a7a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a7a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0a7a3-103">Hämta egenskapen NetWorkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="0a7a3-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a7a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a7a3-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a7a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a7a3-105">DESCRIPTION</span></span>
<span data-ttu-id="0a7a3-106">Cmdleten **Get-AzureRmStorageAccountNetworkRuleSet** hämtar egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="0a7a3-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="0a7a3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a7a3-107">EXAMPLES</span></span>

### <span data-ttu-id="0a7a3-108">Exempel 1: get NetworkRule-egenskapen för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="0a7a3-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="0a7a3-109">Det här kommandot får egenskapen NetworkRule för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="0a7a3-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="0a7a3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a7a3-110">PARAMETERS</span></span>

### <span data-ttu-id="0a7a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a7a3-111">-DefaultProfile</span></span>
<span data-ttu-id="0a7a3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a7a3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a7a3-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="0a7a3-113">-Name</span></span>
<span data-ttu-id="0a7a3-114">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="0a7a3-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="0a7a3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a7a3-115">-ResourceGroupName</span></span>
<span data-ttu-id="0a7a3-116">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="0a7a3-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="0a7a3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a7a3-117">CommonParameters</span></span>
<span data-ttu-id="0a7a3-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a7a3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a7a3-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a7a3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a7a3-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a7a3-120">INPUTS</span></span>

### <span data-ttu-id="0a7a3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0a7a3-121">System.String</span></span>

## <span data-ttu-id="0a7a3-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a7a3-122">OUTPUTS</span></span>

### <span data-ttu-id="0a7a3-123">Microsoft. Azure. commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a7a3-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="0a7a3-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a7a3-124">NOTES</span></span>

## <span data-ttu-id="0a7a3-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a7a3-125">RELATED LINKS</span></span>
