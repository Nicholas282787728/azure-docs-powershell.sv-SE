---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 73384827b5af2b3370eca1eee5a90066a89b8e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920761"
---
# <span data-ttu-id="e98f7-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e98f7-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="e98f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e98f7-102">SYNOPSIS</span></span>
<span data-ttu-id="e98f7-103">Lägger till en åtgärd i objektet inManagementPolicy eller skapar ett ManagementPolicy-objekt med åtgärden.</span><span class="sxs-lookup"><span data-stu-id="e98f7-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="e98f7-104">Objektet kan användas i New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="e98f7-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="e98f7-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e98f7-105">SYNTAX</span></span>

### <span data-ttu-id="e98f7-106">BaseBlob (standard)</span><span class="sxs-lookup"><span data-stu-id="e98f7-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e98f7-107">Generering</span><span class="sxs-lookup"><span data-stu-id="e98f7-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e98f7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e98f7-108">DESCRIPTION</span></span>
<span data-ttu-id="e98f7-109">Cmdleten **Add-AzStorageAccountManagementPolicyAction** lägger till en åtgärd i objektet ManagementPolicy eller skapar ett objekt med åtgärds gruppen ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="e98f7-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="e98f7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e98f7-110">EXAMPLES</span></span>

### <span data-ttu-id="e98f7-111">Exempel 1: skapar ett ManagementPolicy-objekt med 4 åtgärder och sedan lägga till det i en hanterings princip regel och ange ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="e98f7-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="e98f7-112">Det första kommandot Skapa ett ManagementPolicy åtgärds grupp objekt, följande 3 kommandon lägger till 3 åtgärder till objektet.</span><span class="sxs-lookup"><span data-stu-id="e98f7-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="e98f7-113">Lägg sedan till den i en hanterings princip regel och ange ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e98f7-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="e98f7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e98f7-114">PARAMETERS</span></span>

### <span data-ttu-id="e98f7-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="e98f7-115">-BaseBlobAction</span></span>
<span data-ttu-id="e98f7-116">Hanterings princip åtgärd för baseblob.</span><span class="sxs-lookup"><span data-stu-id="e98f7-116">The management policy action for baseblob.</span></span>

```yaml
Type: System.String
Parameter Sets: BaseBlob
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98f7-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="e98f7-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="e98f7-118">Ett heltals värde som anger åldern i dagar efter att det har skapats.</span><span class="sxs-lookup"><span data-stu-id="e98f7-118">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98f7-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="e98f7-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="e98f7-120">Heltals värde som anger åldern i dagar efter den senaste modifieringen.</span><span class="sxs-lookup"><span data-stu-id="e98f7-120">Integer value indicating the age in days after last modification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BaseBlob
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98f7-121">-DefaultProfile</span></span>
<span data-ttu-id="e98f7-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e98f7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e98f7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e98f7-123">-InputObject</span></span>
<span data-ttu-id="e98f7-124">Om du anger indata för instruktionen ManagementPolicy kommer åtgärden till objektet indata.</span><span class="sxs-lookup"><span data-stu-id="e98f7-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="e98f7-125">Om ingen inmatning skapas ett nytt action-objekt.</span><span class="sxs-lookup"><span data-stu-id="e98f7-125">If not input, will create a new action object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e98f7-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="e98f7-126">-SnapshotAction</span></span>
<span data-ttu-id="e98f7-127">Hanterings princip åtgärden för ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="e98f7-127">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98f7-128">CommonParameters</span></span>
<span data-ttu-id="e98f7-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e98f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98f7-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e98f7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98f7-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e98f7-131">INPUTS</span></span>

### <span data-ttu-id="e98f7-132">Microsoft. Azure. commands. Management. Storage. Models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="e98f7-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="e98f7-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e98f7-133">OUTPUTS</span></span>

### <span data-ttu-id="e98f7-134">Microsoft. Azure. commands. Management. Storage. Models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="e98f7-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="e98f7-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e98f7-135">NOTES</span></span>

## <span data-ttu-id="e98f7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e98f7-136">RELATED LINKS</span></span>
