---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 76238516065dffc7a8a38ee6ad025f67d54b47c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575908"
---
# <span data-ttu-id="79d11-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="79d11-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="79d11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79d11-102">SYNOPSIS</span></span>
<span data-ttu-id="79d11-103">Aktiverar säkerhets kopiering av ett objekt med en angiven säkerhets policy för säkerhet.</span><span class="sxs-lookup"><span data-stu-id="79d11-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79d11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79d11-104">SYNTAX</span></span>

### <span data-ttu-id="79d11-105">AzureVMComputeEnableProtection (standard)</span><span class="sxs-lookup"><span data-stu-id="79d11-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79d11-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="79d11-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79d11-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="79d11-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79d11-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79d11-108">DESCRIPTION</span></span>
<span data-ttu-id="79d11-109">Cmdleten **Enable-AzureRmRecoveryServicesBackupProtection** anger Azure säkerhets kopierings princip för ett objekt.</span><span class="sxs-lookup"><span data-stu-id="79d11-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="79d11-110">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79d11-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="79d11-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79d11-111">EXAMPLES</span></span>

### <span data-ttu-id="79d11-112">Exempel 1: Aktivera säkerhets kopierings skydd för ett objekt</span><span class="sxs-lookup"><span data-stu-id="79d11-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="79d11-113">Den första cmdleten får ett standard princip objekt och lagrar det sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="79d11-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="79d11-114">Den andra cmdleten ställer in säkerhets kopierings skydds principen för den virtuella dator ARM med namnet V2VM med principen i $Pol.</span><span class="sxs-lookup"><span data-stu-id="79d11-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="79d11-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79d11-115">PARAMETERS</span></span>

### <span data-ttu-id="79d11-116">-Objekt</span><span class="sxs-lookup"><span data-stu-id="79d11-116">-Item</span></span>
<span data-ttu-id="79d11-117">Anger det säkerhets kopie objekt som denna cmdlet aktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="79d11-117">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="79d11-118">För att få en **AzureRmRecoveryServicesBackupItem** , Använd cmdleten Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="79d11-118">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79d11-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="79d11-119">-Name</span></span>
<span data-ttu-id="79d11-120">Anger namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="79d11-120">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79d11-121">-Princip</span><span class="sxs-lookup"><span data-stu-id="79d11-121">-Policy</span></span>
<span data-ttu-id="79d11-122">Anger skydds princip som denna cmdlet associerar med ett objekt.</span><span class="sxs-lookup"><span data-stu-id="79d11-122">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="79d11-123">Använd Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet för att få ett **AzureRmRecoveryServicesBackupProtectionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="79d11-123">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d11-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79d11-124">-ResourceGroupName</span></span>
<span data-ttu-id="79d11-125">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="79d11-125">Specifies the name of the resource group.</span></span>
<span data-ttu-id="79d11-126">Ange endast den här parametern för virtuella ARM datorer.</span><span class="sxs-lookup"><span data-stu-id="79d11-126">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79d11-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="79d11-127">-ServiceName</span></span>
<span data-ttu-id="79d11-128">Anger tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="79d11-128">Specifies the service name.</span></span>
<span data-ttu-id="79d11-129">Ange endast den här parametern för virtuella ASM-datorer.</span><span class="sxs-lookup"><span data-stu-id="79d11-129">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79d11-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d11-130">-DefaultProfile</span></span>
<span data-ttu-id="79d11-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79d11-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79d11-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d11-132">CommonParameters</span></span>
<span data-ttu-id="79d11-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79d11-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d11-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79d11-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d11-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79d11-135">INPUTS</span></span>

### <span data-ttu-id="79d11-136">ItemBase</span><span class="sxs-lookup"><span data-stu-id="79d11-136">ItemBase</span></span>
<span data-ttu-id="79d11-137">Parametern ' item ' godkänner värdet av typen ' ItemBase ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="79d11-137">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="79d11-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79d11-138">OUTPUTS</span></span>

### <span data-ttu-id="79d11-139">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="79d11-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="79d11-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79d11-140">NOTES</span></span>

## <span data-ttu-id="79d11-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79d11-141">RELATED LINKS</span></span>

[<span data-ttu-id="79d11-142">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="79d11-142">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="79d11-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="79d11-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


