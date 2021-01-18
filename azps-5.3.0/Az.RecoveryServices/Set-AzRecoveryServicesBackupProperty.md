---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 27b783234f9f38f7445940ceb9969b6bc7fb6273
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523972"
---
# <span data-ttu-id="24d31-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="24d31-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="24d31-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24d31-102">SYNOPSIS</span></span>
<span data-ttu-id="24d31-103">Anger egenskaper för säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="24d31-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="24d31-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24d31-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24d31-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24d31-105">DESCRIPTION</span></span>
<span data-ttu-id="24d31-106">Cmdleten **set-AzRecoveryServicesBackupProperty** anger egenskaper för säkerhets kopierings lagring för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="24d31-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="24d31-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24d31-107">EXAMPLES</span></span>

### <span data-ttu-id="24d31-108">Exempel 1: Ange redundant lagrings utrymme för ett valv</span><span class="sxs-lookup"><span data-stu-id="24d31-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="24d31-109">Det första kommandot får valvet med namnet TestVault och lagrar det sedan i variabeln $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="24d31-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="24d31-110">Det andra kommandot ställer in redundans för säkerhets kopiering för $Vault 01 till redundant.</span><span class="sxs-lookup"><span data-stu-id="24d31-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="24d31-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24d31-111">PARAMETERS</span></span>

### <span data-ttu-id="24d31-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="24d31-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="24d31-113">Anger typen av redundans för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="24d31-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d31-114">-DefaultProfile</span></span>
<span data-ttu-id="24d31-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24d31-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24d31-116">-Valv</span><span class="sxs-lookup"><span data-stu-id="24d31-116">-Vault</span></span>
<span data-ttu-id="24d31-117">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="24d31-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="24d31-118">Valvet måste vara ett **AzureRmRecoveryServicesVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="24d31-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24d31-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24d31-119">-Confirm</span></span>
<span data-ttu-id="24d31-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24d31-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d31-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d31-121">-WhatIf</span></span>
<span data-ttu-id="24d31-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24d31-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="24d31-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d31-123">CommonParameters</span></span>
<span data-ttu-id="24d31-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d31-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d31-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24d31-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d31-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24d31-126">INPUTS</span></span>

### <span data-ttu-id="24d31-127">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="24d31-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="24d31-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24d31-128">OUTPUTS</span></span>

### <span data-ttu-id="24d31-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="24d31-129">System.Void</span></span>

## <span data-ttu-id="24d31-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24d31-130">NOTES</span></span>

## <span data-ttu-id="24d31-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24d31-131">RELATED LINKS</span></span>

[<span data-ttu-id="24d31-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="24d31-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="24d31-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="24d31-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


