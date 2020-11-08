---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 3752e520c3637ffa1e08bfd89d03c6caeebd4e18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919398"
---
# <span data-ttu-id="9f7ec-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="9f7ec-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="9f7ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="9f7ec-103">Varning! om du avregistrerar en server kommer alla Server slut punkter att tas bort från den här servern.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="9f7ec-104">Det här kommandot avregistrerar en server från tjänsten Storage Sync.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="9f7ec-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f7ec-105">SYNTAX</span></span>

### <span data-ttu-id="9f7ec-106">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9f7ec-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f7ec-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f7ec-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f7ec-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f7ec-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f7ec-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f7ec-109">DESCRIPTION</span></span>
<span data-ttu-id="9f7ec-110">Det här kommandot avregistrerar en server från Storage Sync-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="9f7ec-111">Varning! om du avregistrerar en server kommer alla Server slut punkter att tas bort från den här servern.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="9f7ec-112">Den bör bara anropas om du är säker på att det inte finns någon sökväg på den här servern längre.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="9f7ec-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f7ec-113">EXAMPLES</span></span>

### <span data-ttu-id="9f7ec-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9f7ec-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="9f7ec-115">Det här kommandot avregistrerar servern och skapar borttagning av alla Server slut punkter på servern.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="9f7ec-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f7ec-116">PARAMETERS</span></span>

### <span data-ttu-id="9f7ec-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f7ec-117">-AsJob</span></span>
<span data-ttu-id="9f7ec-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9f7ec-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f7ec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f7ec-119">-DefaultProfile</span></span>
<span data-ttu-id="9f7ec-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f7ec-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9f7ec-121">-Force</span></span>
<span data-ttu-id="9f7ec-122">Försörjning-Force för att hoppa över bekräftelsen av det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-122">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7ec-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f7ec-123">-InputObject</span></span>
<span data-ttu-id="9f7ec-124">RegisteredServer-textobjekt, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7ec-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f7ec-125">-PassThru</span></span>
<span data-ttu-id="9f7ec-126">I normal körning returnerar denna cmdlet inget värde vid framgång.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="9f7ec-127">Om du anger parametern PassThru, skriver cmdleten ett värde till pipeline efter att körningen lyckats.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="9f7ec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f7ec-128">-ResourceGroupName</span></span>
<span data-ttu-id="9f7ec-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f7ec-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f7ec-130">-ResourceId</span></span>
<span data-ttu-id="9f7ec-131">RegisteredServer-resurs-ID</span><span class="sxs-lookup"><span data-stu-id="9f7ec-131">RegisteredServer Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7ec-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="9f7ec-132">-ServerId</span></span>
<span data-ttu-id="9f7ec-133">Namn på RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-133">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: StringParameterSet
Aliases: RegisteredServerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f7ec-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9f7ec-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="9f7ec-135">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-135">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f7ec-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9f7ec-136">-Confirm</span></span>
<span data-ttu-id="9f7ec-137">Här visas en uppmaning om att bekräfta innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f7ec-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f7ec-138">-WhatIf</span></span>
<span data-ttu-id="9f7ec-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f7ec-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f7ec-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f7ec-141">CommonParameters</span></span>
<span data-ttu-id="9f7ec-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f7ec-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f7ec-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f7ec-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f7ec-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f7ec-144">INPUTS</span></span>

### <span data-ttu-id="9f7ec-145">Microsoft. Azure. commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="9f7ec-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="9f7ec-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9f7ec-146">System.String</span></span>

### <span data-ttu-id="9f7ec-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9f7ec-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9f7ec-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f7ec-148">OUTPUTS</span></span>

### <span data-ttu-id="9f7ec-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="9f7ec-149">System.Object</span></span>
## <span data-ttu-id="9f7ec-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f7ec-150">NOTES</span></span>

## <span data-ttu-id="9f7ec-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f7ec-151">RELATED LINKS</span></span>