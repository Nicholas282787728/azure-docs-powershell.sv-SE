---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c216765657cc87c958cc20dd0f2014f0e1c16970
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746277"
---
# <span data-ttu-id="da5a7-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="da5a7-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="da5a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="da5a7-103">Skapar eller uppdaterar ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="da5a7-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="da5a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da5a7-104">SYNTAX</span></span>

### <span data-ttu-id="da5a7-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="da5a7-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da5a7-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="da5a7-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da5a7-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="da5a7-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da5a7-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="da5a7-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da5a7-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="da5a7-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da5a7-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="da5a7-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da5a7-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="da5a7-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da5a7-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="da5a7-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da5a7-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da5a7-113">DESCRIPTION</span></span>
<span data-ttu-id="da5a7-114">Cmdleten **set-AzRmStorageContainerImmutabilityPolicy** skapar eller uppdaterar ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="da5a7-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="da5a7-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da5a7-115">EXAMPLES</span></span>

### <span data-ttu-id="da5a7-116">Exempel 1: skapa eller uppdatera ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="da5a7-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="da5a7-117">Det här kommandot skapar eller uppdaterar ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="da5a7-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="da5a7-118">Exempel 2: Förläng ImmutabilityPolicy av en lagrings-behållare med lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="da5a7-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="da5a7-119">Det här kommandot utökar ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt.</span><span class="sxs-lookup"><span data-stu-id="da5a7-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="da5a7-120">Utökade ImmutabilityPolicy kan bara köras när ImmutabilityPolicy är låst.</span><span class="sxs-lookup"><span data-stu-id="da5a7-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="da5a7-121">Exempel 3: uppdatera ImmutabilityPolicyof en BLOB-behållare för lagring</span><span class="sxs-lookup"><span data-stu-id="da5a7-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="da5a7-122">Det här kommandot uppdaterar ImmutabilityPolicy för en lagrings-behållare med lagrings behållar objekt 2 gånger, först till ImmutabilityPeriod 12 dagar utan etag, och sedan till ImmutabilityPeriod nio dagar med etag.</span><span class="sxs-lookup"><span data-stu-id="da5a7-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="da5a7-123">Exempel 4: Förläng ImmutabilityPolicy av en lagrings-behållare med ImmutabilityPolicy-objekt</span><span class="sxs-lookup"><span data-stu-id="da5a7-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="da5a7-124">Det här kommandot utökar ImmutabilityPolicy för en lagrings-behållare med ImmutabilityPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="da5a7-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="da5a7-125">Utökade ImmutabilityPolicy kan bara köras när ImmutabilityPolicy är låst.</span><span class="sxs-lookup"><span data-stu-id="da5a7-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="da5a7-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da5a7-126">PARAMETERS</span></span>

### <span data-ttu-id="da5a7-127">-Container</span><span class="sxs-lookup"><span data-stu-id="da5a7-127">-Container</span></span>
<span data-ttu-id="da5a7-128">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="da5a7-128">Storage container object</span></span>

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

### <span data-ttu-id="da5a7-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="da5a7-129">-ContainerName</span></span>
<span data-ttu-id="da5a7-130">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="da5a7-130">Container Name</span></span>

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

### <span data-ttu-id="da5a7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da5a7-131">-DefaultProfile</span></span>
<span data-ttu-id="da5a7-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da5a7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da5a7-133">-Etag</span><span class="sxs-lookup"><span data-stu-id="da5a7-133">-Etag</span></span>
<span data-ttu-id="da5a7-134">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="da5a7-134">Immutability policy etag.</span></span> <span data-ttu-id="da5a7-135">Om-ExtendPolicy inte anges är etag valfri; Else etag krävs.</span><span class="sxs-lookup"><span data-stu-id="da5a7-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="da5a7-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="da5a7-136">-ExtendPolicy</span></span>
<span data-ttu-id="da5a7-137">Ange ExtendPolicy för att utöka en befintlig ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="da5a7-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="da5a7-138">När ImmutabilityPolicy är låst kan den bara utökas.</span><span class="sxs-lookup"><span data-stu-id="da5a7-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="da5a7-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="da5a7-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="da5a7-140">Immutability-perioden sedan den skapades i dagar.</span><span class="sxs-lookup"><span data-stu-id="da5a7-140">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da5a7-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da5a7-141">-InputObject</span></span>
<span data-ttu-id="da5a7-142">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="da5a7-142">Container Name</span></span>

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

### <span data-ttu-id="da5a7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da5a7-143">-ResourceGroupName</span></span>
<span data-ttu-id="da5a7-144">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="da5a7-144">Resource Group Name.</span></span>

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

### <span data-ttu-id="da5a7-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="da5a7-145">-StorageAccount</span></span>
<span data-ttu-id="da5a7-146">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="da5a7-146">Storage account object</span></span>

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

### <span data-ttu-id="da5a7-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="da5a7-147">-StorageAccountName</span></span>
<span data-ttu-id="da5a7-148">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="da5a7-148">Storage Account Name.</span></span>

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

### <span data-ttu-id="da5a7-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da5a7-149">-Confirm</span></span>
<span data-ttu-id="da5a7-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da5a7-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da5a7-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da5a7-151">-WhatIf</span></span>
<span data-ttu-id="da5a7-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da5a7-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da5a7-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da5a7-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da5a7-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da5a7-154">CommonParameters</span></span>
<span data-ttu-id="da5a7-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da5a7-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da5a7-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da5a7-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da5a7-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da5a7-157">INPUTS</span></span>

### <span data-ttu-id="da5a7-158">System. String</span><span class="sxs-lookup"><span data-stu-id="da5a7-158">System.String</span></span>

### <span data-ttu-id="da5a7-159">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="da5a7-159">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="da5a7-160">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="da5a7-160">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="da5a7-161">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="da5a7-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="da5a7-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da5a7-162">OUTPUTS</span></span>

### <span data-ttu-id="da5a7-163">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="da5a7-163">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="da5a7-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da5a7-164">NOTES</span></span>

## <span data-ttu-id="da5a7-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da5a7-165">RELATED LINKS</span></span>
