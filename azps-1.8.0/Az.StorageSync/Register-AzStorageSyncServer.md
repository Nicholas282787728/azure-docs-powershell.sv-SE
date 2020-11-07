---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: edfeebf9781c40b44a5a06db407757a5e2f5d2a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746210"
---
# <span data-ttu-id="be3ec-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="be3ec-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="be3ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="be3ec-103">Det här kommandot registrerar en server i en lagrings tjänst som skapar en förtroende relation.</span><span class="sxs-lookup"><span data-stu-id="be3ec-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="be3ec-104">PowerShell eller Azure-portalen kan sedan användas för att konfigurera synkronisering på den här servern.</span><span class="sxs-lookup"><span data-stu-id="be3ec-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="be3ec-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be3ec-105">SYNTAX</span></span>

### <span data-ttu-id="be3ec-106">ObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="be3ec-106">ObjectParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be3ec-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="be3ec-107">StringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be3ec-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="be3ec-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be3ec-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be3ec-109">DESCRIPTION</span></span>
<span data-ttu-id="be3ec-110">Det här kommandot registrerar en server i en lagrings synkroniseringstjänst, den översta resursen för Azure-filsynkronisering. En förtroende relation mellan server-och Storage Sync-tjänsten skapas som säkerställer säkra kanaler för data överföring och-hantering.</span><span class="sxs-lookup"><span data-stu-id="be3ec-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="be3ec-111">PowerShell eller Azure-portalen kan sedan användas för att konfigurera vilka synkroniseringar som ska göras på den här servern.</span><span class="sxs-lookup"><span data-stu-id="be3ec-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="be3ec-112">En server kan bara vara registrerad på en enda lagrings synkroniseringstjänst.</span><span class="sxs-lookup"><span data-stu-id="be3ec-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="be3ec-113">Om servrar någonsin behöver delta i synkroniseringen av samma uppsättning filer registrerar du dem på samma synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="be3ec-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="be3ec-114">Kommandot måste köras lokalt på den server som ska registreras – antingen körs direkt eller via en fjärrsession med PowerShell.</span><span class="sxs-lookup"><span data-stu-id="be3ec-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="be3ec-115">Det går inte att acceptera ett fjärrdator objekt.</span><span class="sxs-lookup"><span data-stu-id="be3ec-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="be3ec-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be3ec-116">EXAMPLES</span></span>

### <span data-ttu-id="be3ec-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="be3ec-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="be3ec-118">Det här kommandot registrerar den lokala servern som kommandot körs på.</span><span class="sxs-lookup"><span data-stu-id="be3ec-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="be3ec-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be3ec-119">PARAMETERS</span></span>

### <span data-ttu-id="be3ec-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be3ec-120">-AsJob</span></span>
<span data-ttu-id="be3ec-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="be3ec-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be3ec-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be3ec-122">-DefaultProfile</span></span>
<span data-ttu-id="be3ec-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="be3ec-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be3ec-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="be3ec-124">-ParentObject</span></span>
<span data-ttu-id="be3ec-125">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="be3ec-125">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be3ec-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="be3ec-126">-ParentResourceId</span></span>
<span data-ttu-id="be3ec-127">Överordnat resurs-ID för StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="be3ec-127">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3ec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be3ec-128">-ResourceGroupName</span></span>
<span data-ttu-id="be3ec-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="be3ec-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="be3ec-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="be3ec-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="be3ec-131">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="be3ec-131">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be3ec-132">CommonParameters</span></span>
<span data-ttu-id="be3ec-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be3ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be3ec-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be3ec-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be3ec-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be3ec-135">INPUTS</span></span>

### <span data-ttu-id="be3ec-136">System. String</span><span class="sxs-lookup"><span data-stu-id="be3ec-136">System.String</span></span>

### <span data-ttu-id="be3ec-137">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="be3ec-137">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="be3ec-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be3ec-138">OUTPUTS</span></span>

### <span data-ttu-id="be3ec-139">Microsoft. Azure. commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="be3ec-139">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="be3ec-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be3ec-140">NOTES</span></span>

## <span data-ttu-id="be3ec-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be3ec-141">RELATED LINKS</span></span>
