---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: 195ef931b942f3dc8a88ede7e3feb31a3b8aa77f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746352"
---
# <span data-ttu-id="80304-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="80304-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="80304-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80304-102">SYNOPSIS</span></span>
<span data-ttu-id="80304-103">Skapar ett ManagementPolicy regel objekt som kan användas i set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="80304-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="80304-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80304-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80304-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80304-105">DESCRIPTION</span></span>
<span data-ttu-id="80304-106">Cmdleten **New-AzStorageAccountManagementPolicyRule** skapar ett ManagementPolicy-regel objekt som kan användas i set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="80304-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="80304-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80304-107">EXAMPLES</span></span>

### <span data-ttu-id="80304-108">Exempel 1: skapar ett ManagementPolicy regel objekt och sedan till ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="80304-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2

PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name rule1 -Action $action -Filter $filter
PS C:\>$rule

Enabled    : True
Name       : rule1
Definition : {
                 "Actions":  {
                                 "BaseBlob":  {
                                                  "TierToCool":  {
                                                                     "DaysAfterModificationGreaterThan":  30
                                                                 },
                                                  "TierToArchive":  {
                                                                        "DaysAfterModificationGreaterThan":  50
                                                                    },
                                                  "Delete":  {
                                                                 "DaysAfterModificationGreaterThan":  100
                                                             }
                                              },
                                 "Snapshot":  {
                                                  "Delete":  {
                                                                 "DaysAfterCreationGreaterThan":  100
                                                             }
                                              }
                             },
                 "Filters":  {
                                 "PrefixMatch":  [
                                                     "blobprefix1",
                                                     "blobprefix2"
                                                 ],
                                 "BlobTypes":  [
                                                   "blockBlob"
                                               ]
                             }
             }

PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="80304-109">Det här kommandot skapar ett ManagementPolicy regel objekt med ett ManagementPolicy-objekt som innehåller fyra åtgärder, ett ManagementPolicy regel filter-objekt och anger sedan regeln till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="80304-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="80304-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80304-110">PARAMETERS</span></span>

### <span data-ttu-id="80304-111">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="80304-111">-Action</span></span>
<span data-ttu-id="80304-112">Ett objekt som definierar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="80304-112">An object that defines the action set.</span></span>
<span data-ttu-id="80304-113">Hämta objektet med cmdlet Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="80304-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80304-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80304-114">-DefaultProfile</span></span>
<span data-ttu-id="80304-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80304-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80304-116">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="80304-116">-Disabled</span></span>
<span data-ttu-id="80304-117">Regeln är avaktiverad om den anges.</span><span class="sxs-lookup"><span data-stu-id="80304-117">The rule is disabled if set it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80304-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="80304-118">-Filter</span></span>
<span data-ttu-id="80304-119">Ett objekt som definierar filter uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="80304-119">An object that defines the filter set.</span></span>
<span data-ttu-id="80304-120">Hämta objektet med cmdlet New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="80304-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80304-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="80304-121">-Name</span></span>
<span data-ttu-id="80304-122">Ett regel namn kan innehålla en kombination av Alfa numeriska tecken.</span><span class="sxs-lookup"><span data-stu-id="80304-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="80304-123">Regel namnet är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="80304-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="80304-124">Det måste vara unikt inom en policy.</span><span class="sxs-lookup"><span data-stu-id="80304-124">It must be unique within a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80304-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80304-125">CommonParameters</span></span>
<span data-ttu-id="80304-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80304-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80304-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80304-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80304-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80304-128">INPUTS</span></span>

### <span data-ttu-id="80304-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="80304-129">None</span></span>

## <span data-ttu-id="80304-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80304-130">OUTPUTS</span></span>

### <span data-ttu-id="80304-131">Microsoft. Azure. commands. Management. Storage. Models. PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="80304-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="80304-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80304-132">NOTES</span></span>

## <span data-ttu-id="80304-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80304-133">RELATED LINKS</span></span>
