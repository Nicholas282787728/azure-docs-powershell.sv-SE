---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 8957a794660750f45f295b77d921e647d368e7dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746984"
---
# <span data-ttu-id="23cb2-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="23cb2-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="23cb2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="23cb2-103">Hämtar principen för avancerat skydd för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="23cb2-103">Gets the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="23cb2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23cb2-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23cb2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23cb2-105">DESCRIPTION</span></span>
<span data-ttu-id="23cb2-106">`Get-AzSecurityAdvancedThreatProtection`Cmdleten skyddas mot ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="23cb2-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage account.</span></span>
<span data-ttu-id="23cb2-107">Ange parametern *ResourceID* för att använda denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23cb2-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="23cb2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23cb2-108">EXAMPLES</span></span>

### <span data-ttu-id="23cb2-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="23cb2-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="23cb2-110">Det här kommandot får principen för avancerat skydd för resurs-ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="23cb2-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="23cb2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23cb2-111">PARAMETERS</span></span>

### <span data-ttu-id="23cb2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cb2-112">-DefaultProfile</span></span>
<span data-ttu-id="23cb2-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="23cb2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23cb2-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23cb2-114">-ResourceId</span></span>
<span data-ttu-id="23cb2-115">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="23cb2-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="23cb2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cb2-116">CommonParameters</span></span>
<span data-ttu-id="23cb2-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cb2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cb2-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23cb2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cb2-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23cb2-119">INPUTS</span></span>

### <span data-ttu-id="23cb2-120">System. String</span><span class="sxs-lookup"><span data-stu-id="23cb2-120">System.String</span></span>

## <span data-ttu-id="23cb2-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23cb2-121">OUTPUTS</span></span>

### <span data-ttu-id="23cb2-122">Microsoft. Azure. commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="23cb2-122">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="23cb2-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23cb2-123">NOTES</span></span>

## <span data-ttu-id="23cb2-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23cb2-124">RELATED LINKS</span></span>
