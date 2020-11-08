---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 3e4cc41bf67eaef505cdeb1e33f84753f20650a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920918"
---
# <span data-ttu-id="10b9a-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="10b9a-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="10b9a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="10b9a-103">Skapar ett regel objekt för ManagementPolicy som kan användas i nya-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="10b9a-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="10b9a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10b9a-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10b9a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="10b9a-106">Cmdleten **New-AzStorageAccountManagementPolicyFilter** skapar ett regel objekt för ManagementPolicy, som kan användas i nya-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="10b9a-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="10b9a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10b9a-107">EXAMPLES</span></span>

### <span data-ttu-id="10b9a-108">Exempel 1: skapar ett regel objekt för ManagementPolicy och lägger till det i en hanterings princip regel och anger ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="10b9a-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="10b9a-109">Det här kommandot skapar ett regel objekt för ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="10b9a-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="10b9a-110">Lägg sedan till den i en hanterings princip regel och ange ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="10b9a-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="10b9a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10b9a-111">PARAMETERS</span></span>

### <span data-ttu-id="10b9a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b9a-112">-DefaultProfile</span></span>
<span data-ttu-id="10b9a-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10b9a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10b9a-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="10b9a-114">-PrefixMatch</span></span>
<span data-ttu-id="10b9a-115">En matris med strängar för prefix som ska matchas.</span><span class="sxs-lookup"><span data-stu-id="10b9a-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="10b9a-116">En prefixlängd måste börja med ett container namn.</span><span class="sxs-lookup"><span data-stu-id="10b9a-116">A prefix string must start with a container name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b9a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b9a-117">CommonParameters</span></span>
<span data-ttu-id="10b9a-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10b9a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b9a-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b9a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b9a-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10b9a-120">INPUTS</span></span>

### <span data-ttu-id="10b9a-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="10b9a-121">None</span></span>

## <span data-ttu-id="10b9a-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10b9a-122">OUTPUTS</span></span>

### <span data-ttu-id="10b9a-123">Microsoft. Azure. commands. Management. Storage. Models. PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="10b9a-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="10b9a-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10b9a-124">NOTES</span></span>

## <span data-ttu-id="10b9a-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10b9a-125">RELATED LINKS</span></span>