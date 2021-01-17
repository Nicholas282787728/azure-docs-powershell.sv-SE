---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403344"
---
# <span data-ttu-id="770da-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="770da-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="770da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="770da-102">SYNOPSIS</span></span>
<span data-ttu-id="770da-103">Skapar eller uppdaterar ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="770da-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="770da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="770da-104">SYNTAX</span></span>

### <span data-ttu-id="770da-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="770da-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770da-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="770da-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770da-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="770da-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770da-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="770da-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770da-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="770da-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770da-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="770da-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770da-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="770da-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="770da-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="770da-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="770da-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="770da-113">DESCRIPTION</span></span>
<span data-ttu-id="770da-114">Cmdleten **set-AzRmStorageContainerImmutabilityPolicy** skapar eller uppdaterar ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="770da-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="770da-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="770da-115">EXAMPLES</span></span>

### <span data-ttu-id="770da-116">Exempel 1: skapa eller uppdatera ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="770da-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="770da-117">Det här kommandot skapar eller uppdaterar ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="770da-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="770da-118">Exempel 2: Förläng ImmutabilityPolicy av en lagrings-behållare med lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="770da-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="770da-119">Det här kommandot utökar ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt.</span><span class="sxs-lookup"><span data-stu-id="770da-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="770da-120">Utökade ImmutabilityPolicy kan bara köras när ImmutabilityPolicy är låst.</span><span class="sxs-lookup"><span data-stu-id="770da-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="770da-121">Exempel 3: uppdatera ImmutabilityPolicy för en lagrings-behållare</span><span class="sxs-lookup"><span data-stu-id="770da-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="770da-122">Det här kommandot uppdaterar ImmutabilityPolicy för en lagrings-behållare med lagrings behållar objekt 3 gånger: första till ImmutabilityPeriod 12 dagar utan etag och sedan till ImmutabilityPeriod nio dagar med etag och slutligen aktive rad AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="770da-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="770da-123">Exempel 4: Förläng ImmutabilityPolicy av en lagrings-behållare med ImmutabilityPolicy-objekt</span><span class="sxs-lookup"><span data-stu-id="770da-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="770da-124">Det här kommandot utökar ImmutabilityPolicy för en lagrings-behållare med ImmutabilityPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="770da-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="770da-125">Utökade ImmutabilityPolicy kan bara köras när ImmutabilityPolicy är låst.</span><span class="sxs-lookup"><span data-stu-id="770da-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="770da-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="770da-126">PARAMETERS</span></span>

### <span data-ttu-id="770da-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="770da-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="770da-128">Den här egenskapen kan bara ändras för olåsta tidsbaserade bevarande principer.</span><span class="sxs-lookup"><span data-stu-id="770da-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="770da-129">När den här egenskapen är aktive rad kan nya block skrivas till en tilläggs-BLOB medan immutability skydd och efterlevnad upprätthålls.</span><span class="sxs-lookup"><span data-stu-id="770da-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="770da-130">Det går bara att lägga till nya block och befintliga block kan inte ändras eller tas bort.</span><span class="sxs-lookup"><span data-stu-id="770da-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770da-131">-Container</span><span class="sxs-lookup"><span data-stu-id="770da-131">-Container</span></span>
<span data-ttu-id="770da-132">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="770da-132">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="770da-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="770da-133">-ContainerName</span></span>
<span data-ttu-id="770da-134">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="770da-134">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="770da-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770da-135">-DefaultProfile</span></span>
<span data-ttu-id="770da-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="770da-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="770da-137">-Etag</span><span class="sxs-lookup"><span data-stu-id="770da-137">-Etag</span></span>
<span data-ttu-id="770da-138">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="770da-138">Immutability policy etag.</span></span> <span data-ttu-id="770da-139">Om-ExtendPolicy inte anges är etag valfri; Else etag krävs.</span><span class="sxs-lookup"><span data-stu-id="770da-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770da-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="770da-140">-ExtendPolicy</span></span>
<span data-ttu-id="770da-141">Ange ExtendPolicy för att utöka en befintlig ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="770da-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="770da-142">När ImmutabilityPolicy är låst kan den bara utökas.</span><span class="sxs-lookup"><span data-stu-id="770da-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770da-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="770da-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="770da-144">Immutability-perioden sedan den skapades i dagar.</span><span class="sxs-lookup"><span data-stu-id="770da-144">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770da-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="770da-145">-InputObject</span></span>
<span data-ttu-id="770da-146">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="770da-146">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="770da-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770da-147">-ResourceGroupName</span></span>
<span data-ttu-id="770da-148">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="770da-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770da-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="770da-149">-StorageAccount</span></span>
<span data-ttu-id="770da-150">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="770da-150">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="770da-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="770da-151">-StorageAccountName</span></span>
<span data-ttu-id="770da-152">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="770da-152">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770da-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="770da-153">-Confirm</span></span>
<span data-ttu-id="770da-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="770da-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770da-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770da-155">-WhatIf</span></span>
<span data-ttu-id="770da-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="770da-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="770da-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="770da-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770da-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770da-158">CommonParameters</span></span>
<span data-ttu-id="770da-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770da-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770da-160">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="770da-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770da-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="770da-161">INPUTS</span></span>

### <span data-ttu-id="770da-162">System. String</span><span class="sxs-lookup"><span data-stu-id="770da-162">System.String</span></span>

### <span data-ttu-id="770da-163">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="770da-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="770da-164">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="770da-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="770da-165">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="770da-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="770da-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="770da-166">OUTPUTS</span></span>

### <span data-ttu-id="770da-167">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="770da-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="770da-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="770da-168">NOTES</span></span>

## <span data-ttu-id="770da-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="770da-169">RELATED LINKS</span></span>
