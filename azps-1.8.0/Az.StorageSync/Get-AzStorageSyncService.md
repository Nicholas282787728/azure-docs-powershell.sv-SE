---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: c724527b380e0004d30e0790024634bcc6ce550d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746227"
---
# <span data-ttu-id="959b6-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="959b6-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="959b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="959b6-102">SYNOPSIS</span></span>
<span data-ttu-id="959b6-103">Det här kommandot visar alla lagrings Sync-tjänster i ett givet omfång av abonnemang/resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="959b6-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="959b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="959b6-104">SYNTAX</span></span>

### <span data-ttu-id="959b6-105">ParentStringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="959b6-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="959b6-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="959b6-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="959b6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="959b6-107">DESCRIPTION</span></span>
<span data-ttu-id="959b6-108">Det här kommandot visar alla lagrings Sync-tjänster i ett givet omfång av abonnemang/resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="959b6-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="959b6-109">Den kan också användas för att lista attributen för varje lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="959b6-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="959b6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="959b6-110">EXAMPLES</span></span>

### <span data-ttu-id="959b6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="959b6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="959b6-112">Det här kommandot listar alla resurser för lagrings tjänst i en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="959b6-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="959b6-113">Den kan också användas för att lista attributen för varje lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="959b6-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="959b6-114">Ange-StorageSyncServiceName för att returnera ett specifikt nummer.</span><span class="sxs-lookup"><span data-stu-id="959b6-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="959b6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="959b6-115">PARAMETERS</span></span>

### <span data-ttu-id="959b6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="959b6-116">-DefaultProfile</span></span>
<span data-ttu-id="959b6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="959b6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="959b6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="959b6-118">-Name</span></span>
<span data-ttu-id="959b6-119">Namn på Storage Sync-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="959b6-119">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="959b6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="959b6-120">-ResourceGroupName</span></span>
<span data-ttu-id="959b6-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="959b6-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="959b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="959b6-122">CommonParameters</span></span>
<span data-ttu-id="959b6-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="959b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="959b6-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="959b6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="959b6-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="959b6-125">INPUTS</span></span>

### <span data-ttu-id="959b6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="959b6-126">System.String</span></span>

## <span data-ttu-id="959b6-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="959b6-127">OUTPUTS</span></span>

### <span data-ttu-id="959b6-128">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="959b6-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="959b6-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="959b6-129">NOTES</span></span>

## <span data-ttu-id="959b6-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="959b6-130">RELATED LINKS</span></span>
