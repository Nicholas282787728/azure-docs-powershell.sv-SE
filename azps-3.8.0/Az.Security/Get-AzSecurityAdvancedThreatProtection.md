---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: d4d2ae2ae8b09f319efe2f77030c88338b4c40b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092033"
---
# <span data-ttu-id="5fd6d-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5fd6d-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="5fd6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fd6d-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd6d-103">Hämtar principen för avancerat skydd för en lagrings-cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5fd6d-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="5fd6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fd6d-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fd6d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fd6d-105">DESCRIPTION</span></span>
<span data-ttu-id="5fd6d-106">`Get-AzSecurityAdvancedThreatProtection`Cmdleten skyddas mot ett lagrings-cosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="5fd6d-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="5fd6d-107">Ange parametern *ResourceID* för att använda denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fd6d-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="5fd6d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fd6d-108">EXAMPLES</span></span>

### <span data-ttu-id="5fd6d-109">Exempel 1: lagrings konto</span><span class="sxs-lookup"><span data-stu-id="5fd6d-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="5fd6d-110">Det här kommandot får principen för avancerat skydd för resurs-ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="5fd6d-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="5fd6d-111">Exempel 2: CosmosDB-konto</span><span class="sxs-lookup"><span data-stu-id="5fd6d-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="5fd6d-112">Det här kommandot får principen för avancerat skydd för resurs-ID ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="5fd6d-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="5fd6d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fd6d-113">PARAMETERS</span></span>

### <span data-ttu-id="5fd6d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd6d-114">-DefaultProfile</span></span>
<span data-ttu-id="5fd6d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fd6d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fd6d-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fd6d-116">-ResourceId</span></span>
<span data-ttu-id="5fd6d-117">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="5fd6d-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5fd6d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd6d-118">CommonParameters</span></span>
<span data-ttu-id="5fd6d-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fd6d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd6d-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fd6d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd6d-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fd6d-121">INPUTS</span></span>

### <span data-ttu-id="5fd6d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5fd6d-122">System.String</span></span>

## <span data-ttu-id="5fd6d-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fd6d-123">OUTPUTS</span></span>

### <span data-ttu-id="5fd6d-124">Microsoft. Azure. commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5fd6d-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="5fd6d-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fd6d-125">NOTES</span></span>

## <span data-ttu-id="5fd6d-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fd6d-126">RELATED LINKS</span></span>
