---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269577"
---
# <span data-ttu-id="408aa-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="408aa-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="408aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="408aa-102">SYNOPSIS</span></span>
<span data-ttu-id="408aa-103">Hämtar eller visar en lösenordsreplikeringsprincip för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="408aa-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="408aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="408aa-104">SYNTAX</span></span>

### <span data-ttu-id="408aa-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="408aa-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="408aa-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="408aa-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="408aa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="408aa-107">DESCRIPTION</span></span>
<span data-ttu-id="408aa-108">Cmdleten **Get-AzStorageObjectReplicationPolicy** hämtar eller listar objektets replikeringsprincip för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="408aa-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="408aa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="408aa-109">EXAMPLES</span></span>

### <span data-ttu-id="408aa-110">Exempel 1: Hämta en princip för lösenordsreplikering med specifika princip-ID och visa dess regler.</span><span class="sxs-lookup"><span data-stu-id="408aa-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
```
PS C:\> $policy = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId 56bfa11c-81ef-4f8d-b307-5e5386e16fba

PS C:\> $policy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> $policy.Rules

RuleId                               SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------                               --------------- -------------------- ------------------- -----------------------
d3d39a01-8d92-40e5-849f-e56209ae5cf5 src1            dest1                {}                                         
2407de9a-3301-4656-858f-359d185565e0 src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="408aa-111">Det här kommandot får en lösenordsreplikeringsprincip med ett visst princip-ID och visar dess regler.</span><span class="sxs-lookup"><span data-stu-id="408aa-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="408aa-112">Exempel 2: Visa en lista över objekt replikeringsprinciper från ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="408aa-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="408aa-113">Det här kommandot listar en lösenordsreplikeringsprincip från ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="408aa-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="408aa-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="408aa-114">PARAMETERS</span></span>

### <span data-ttu-id="408aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408aa-115">-DefaultProfile</span></span>
<span data-ttu-id="408aa-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="408aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="408aa-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="408aa-117">-PolicyId</span></span>
<span data-ttu-id="408aa-118">ID för principobjektet för objekt.</span><span class="sxs-lookup"><span data-stu-id="408aa-118">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408aa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="408aa-119">-ResourceGroupName</span></span>
<span data-ttu-id="408aa-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="408aa-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408aa-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="408aa-121">-StorageAccount</span></span>
<span data-ttu-id="408aa-122">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="408aa-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="408aa-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="408aa-123">-StorageAccountName</span></span>
<span data-ttu-id="408aa-124">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="408aa-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408aa-125">CommonParameters</span></span>
<span data-ttu-id="408aa-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408aa-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="408aa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408aa-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="408aa-128">INPUTS</span></span>

### <span data-ttu-id="408aa-129">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="408aa-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="408aa-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="408aa-130">OUTPUTS</span></span>

### <span data-ttu-id="408aa-131">Microsoft. Azure. commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="408aa-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="408aa-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="408aa-132">NOTES</span></span>

## <span data-ttu-id="408aa-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="408aa-133">RELATED LINKS</span></span>
