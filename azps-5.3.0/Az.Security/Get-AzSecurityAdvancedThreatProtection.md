---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525663"
---
# <span data-ttu-id="ad8f6-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ad8f6-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="ad8f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad8f6-103">Hämtar principen för avancerat skydd för en lagrings-cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ad8f6-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="ad8f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad8f6-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad8f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad8f6-105">DESCRIPTION</span></span>
<span data-ttu-id="ad8f6-106">`Get-AzSecurityAdvancedThreatProtection`Cmdleten skyddas mot ett lagrings-cosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="ad8f6-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="ad8f6-107">Ange parametern *ResourceID* för att använda denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad8f6-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="ad8f6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad8f6-108">EXAMPLES</span></span>

### <span data-ttu-id="ad8f6-109">Exempel 1: lagrings konto</span><span class="sxs-lookup"><span data-stu-id="ad8f6-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="ad8f6-110">Det här kommandot får principen för avancerat skydd för resurs-ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="ad8f6-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="ad8f6-111">Exempel 2: CosmosDB-konto</span><span class="sxs-lookup"><span data-stu-id="ad8f6-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="ad8f6-112">Det här kommandot får principen för avancerat skydd för resurs-ID ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="ad8f6-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="ad8f6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad8f6-113">PARAMETERS</span></span>

### <span data-ttu-id="ad8f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad8f6-114">-DefaultProfile</span></span>
<span data-ttu-id="ad8f6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad8f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad8f6-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad8f6-116">-ResourceId</span></span>
<span data-ttu-id="ad8f6-117">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="ad8f6-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="ad8f6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad8f6-118">CommonParameters</span></span>
<span data-ttu-id="ad8f6-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad8f6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad8f6-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad8f6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad8f6-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad8f6-121">INPUTS</span></span>

### <span data-ttu-id="ad8f6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ad8f6-122">System.String</span></span>

## <span data-ttu-id="ad8f6-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad8f6-123">OUTPUTS</span></span>

### <span data-ttu-id="ad8f6-124">Microsoft. Azure. commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ad8f6-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="ad8f6-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad8f6-125">NOTES</span></span>

## <span data-ttu-id="ad8f6-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad8f6-126">RELATED LINKS</span></span>
