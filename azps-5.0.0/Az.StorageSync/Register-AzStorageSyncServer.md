---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: bb1ce6f9ff7e846c2f485665cafad700fa4c825b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271689"
---
# <span data-ttu-id="26f8a-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="26f8a-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="26f8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="26f8a-103">Det här kommandot registrerar en server i en lagrings tjänst som skapar en förtroende relation.</span><span class="sxs-lookup"><span data-stu-id="26f8a-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="26f8a-104">PowerShell eller Azure-portalen kan sedan användas för att konfigurera synkronisering på den här servern.</span><span class="sxs-lookup"><span data-stu-id="26f8a-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="26f8a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26f8a-105">SYNTAX</span></span>

### <span data-ttu-id="26f8a-106">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="26f8a-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f8a-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f8a-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f8a-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f8a-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26f8a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26f8a-109">DESCRIPTION</span></span>
<span data-ttu-id="26f8a-110">Det här kommandot registrerar en server i en lagrings synkroniseringstjänst, den översta resursen för Azure-filsynkronisering. En förtroende relation mellan server-och Storage Sync-tjänsten skapas som säkerställer säkra kanaler för data överföring och-hantering.</span><span class="sxs-lookup"><span data-stu-id="26f8a-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="26f8a-111">PowerShell eller Azure-portalen kan sedan användas för att konfigurera vilka synkroniseringar som ska göras på den här servern.</span><span class="sxs-lookup"><span data-stu-id="26f8a-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="26f8a-112">En server kan bara vara registrerad på en enda lagrings synkroniseringstjänst.</span><span class="sxs-lookup"><span data-stu-id="26f8a-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="26f8a-113">Om servrar någonsin behöver delta i synkroniseringen av samma uppsättning filer registrerar du dem på samma synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="26f8a-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="26f8a-114">Kommandot måste köras lokalt på den server som ska registreras – antingen körs direkt eller via en fjärrsession med PowerShell.</span><span class="sxs-lookup"><span data-stu-id="26f8a-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="26f8a-115">Det går inte att acceptera ett fjärrdator objekt.</span><span class="sxs-lookup"><span data-stu-id="26f8a-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="26f8a-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26f8a-116">EXAMPLES</span></span>

### <span data-ttu-id="26f8a-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="26f8a-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="26f8a-118">Det här kommandot registrerar den lokala servern som kommandot körs på.</span><span class="sxs-lookup"><span data-stu-id="26f8a-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="26f8a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26f8a-119">PARAMETERS</span></span>

### <span data-ttu-id="26f8a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26f8a-120">-AsJob</span></span>
<span data-ttu-id="26f8a-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="26f8a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26f8a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f8a-122">-DefaultProfile</span></span>
<span data-ttu-id="26f8a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26f8a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26f8a-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="26f8a-124">-ParentObject</span></span>
<span data-ttu-id="26f8a-125">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="26f8a-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="26f8a-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="26f8a-126">-ParentResourceId</span></span>
<span data-ttu-id="26f8a-127">Överordnat resurs-ID för StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="26f8a-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="26f8a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f8a-128">-ResourceGroupName</span></span>
<span data-ttu-id="26f8a-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="26f8a-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="26f8a-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="26f8a-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="26f8a-131">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="26f8a-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="26f8a-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="26f8a-132">-Confirm</span></span>
<span data-ttu-id="26f8a-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="26f8a-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f8a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f8a-134">-WhatIf</span></span>
<span data-ttu-id="26f8a-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="26f8a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26f8a-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="26f8a-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f8a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f8a-137">CommonParameters</span></span>
<span data-ttu-id="26f8a-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26f8a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f8a-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f8a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f8a-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26f8a-140">INPUTS</span></span>

### <span data-ttu-id="26f8a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="26f8a-141">System.String</span></span>

### <span data-ttu-id="26f8a-142">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="26f8a-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="26f8a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26f8a-143">OUTPUTS</span></span>

### <span data-ttu-id="26f8a-144">Microsoft. Azure. commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="26f8a-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="26f8a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26f8a-145">NOTES</span></span>

## <span data-ttu-id="26f8a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26f8a-146">RELATED LINKS</span></span>
