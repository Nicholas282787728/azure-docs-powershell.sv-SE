---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 245eb56ea973c1330b7f8b9d32a3f0b9584bd0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756539"
---
# <span data-ttu-id="f43c1-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f43c1-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="f43c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f43c1-102">SYNOPSIS</span></span>
<span data-ttu-id="f43c1-103">Anger tillståndet för en entitet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="f43c1-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f43c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f43c1-104">SYNTAX</span></span>

### <span data-ttu-id="f43c1-105">Avaktiverare (standard)</span><span class="sxs-lookup"><span data-stu-id="f43c1-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f43c1-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="f43c1-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f43c1-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="f43c1-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f43c1-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="f43c1-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f43c1-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f43c1-109">DESCRIPTION</span></span>
<span data-ttu-id="f43c1-110">Cmdleten **set-AzureRmSiteRecoveryProtectionEntity** aktiverar eller inaktiverar skydd för en Azure Site Recovery-enhet.</span><span class="sxs-lookup"><span data-stu-id="f43c1-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="f43c1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f43c1-111">EXAMPLES</span></span>

## <span data-ttu-id="f43c1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f43c1-112">PARAMETERS</span></span>

### <span data-ttu-id="f43c1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f43c1-113">-Force</span></span>
<span data-ttu-id="f43c1-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f43c1-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f43c1-115">-OS</span><span class="sxs-lookup"><span data-stu-id="f43c1-115">-OS</span></span>
<span data-ttu-id="f43c1-116">Anger typen av operativ system.</span><span class="sxs-lookup"><span data-stu-id="f43c1-116">Specifies the operating system type.</span></span>
<span data-ttu-id="f43c1-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f43c1-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f43c1-118">Windows</span><span class="sxs-lookup"><span data-stu-id="f43c1-118">Windows</span></span>
- <span data-ttu-id="f43c1-119">Linux</span><span class="sxs-lookup"><span data-stu-id="f43c1-119">Linux</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43c1-120">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="f43c1-120">-OSDiskName</span></span>
<span data-ttu-id="f43c1-121">Anger namnet på den disk som innehåller operativ systemet.</span><span class="sxs-lookup"><span data-stu-id="f43c1-121">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43c1-122">-Princip</span><span class="sxs-lookup"><span data-stu-id="f43c1-122">-Policy</span></span>
<span data-ttu-id="f43c1-123">Anger principobjektet för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="f43c1-123">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43c1-124">-Skydd</span><span class="sxs-lookup"><span data-stu-id="f43c1-124">-Protection</span></span>
<span data-ttu-id="f43c1-125">Anger om skydd ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="f43c1-125">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="f43c1-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f43c1-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f43c1-127">Aktivering</span><span class="sxs-lookup"><span data-stu-id="f43c1-127">Enable</span></span>
- <span data-ttu-id="f43c1-128">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="f43c1-128">Disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43c1-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f43c1-129">-ProtectionEntity</span></span>
<span data-ttu-id="f43c1-130">Anger objektet skydd.</span><span class="sxs-lookup"><span data-stu-id="f43c1-130">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f43c1-131">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f43c1-131">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f43c1-132">Anger ID för mål Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="f43c1-132">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43c1-133">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f43c1-133">-WaitForCompletion</span></span>
<span data-ttu-id="f43c1-134">Anger att kommandot väntar på slut innan det returneras.</span><span class="sxs-lookup"><span data-stu-id="f43c1-134">Indicates that the command waits for completion before returning.</span></span>

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

### <span data-ttu-id="f43c1-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f43c1-135">-Confirm</span></span>
<span data-ttu-id="f43c1-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f43c1-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43c1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f43c1-137">-WhatIf</span></span>
<span data-ttu-id="f43c1-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f43c1-138">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f43c1-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f43c1-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43c1-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f43c1-140">-DefaultProfile</span></span>
<span data-ttu-id="f43c1-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f43c1-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43c1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f43c1-142">CommonParameters</span></span>
<span data-ttu-id="f43c1-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f43c1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f43c1-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f43c1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f43c1-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f43c1-145">INPUTS</span></span>

### <span data-ttu-id="f43c1-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f43c1-146">ASRProtectionEntity</span></span>
<span data-ttu-id="f43c1-147">Parametern ' ProtectionEntity ' godkänner värdet av typen ' ASRProtectionEntity ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f43c1-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="f43c1-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f43c1-148">OUTPUTS</span></span>

### <span data-ttu-id="f43c1-149">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f43c1-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f43c1-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f43c1-150">NOTES</span></span>

## <span data-ttu-id="f43c1-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f43c1-151">RELATED LINKS</span></span>

[<span data-ttu-id="f43c1-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f43c1-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
