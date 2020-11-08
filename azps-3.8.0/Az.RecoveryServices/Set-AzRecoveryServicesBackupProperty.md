---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 538fe4fe21394c817b7bb2a954fbdbcc2ccfb097
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091251"
---
# <span data-ttu-id="d7764-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="d7764-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="d7764-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7764-102">SYNOPSIS</span></span>
<span data-ttu-id="d7764-103">Anger egenskaper för säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="d7764-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="d7764-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7764-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7764-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7764-105">DESCRIPTION</span></span>
<span data-ttu-id="d7764-106">Cmdleten **set-AzRecoveryServicesBackupProperty** anger egenskaper för säkerhets kopierings lagring för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="d7764-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="d7764-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7764-107">EXAMPLES</span></span>

### <span data-ttu-id="d7764-108">Exempel 1: Ange redundant lagrings utrymme för ett valv</span><span class="sxs-lookup"><span data-stu-id="d7764-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="d7764-109">Det första kommandot får valvet med namnet TestVault och lagrar det sedan i variabeln $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="d7764-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="d7764-110">Det andra kommandot ställer in redundans för säkerhets kopiering för $Vault 01 till redundant.</span><span class="sxs-lookup"><span data-stu-id="d7764-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="d7764-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7764-111">PARAMETERS</span></span>

### <span data-ttu-id="d7764-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="d7764-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="d7764-113">Anger typen av redundans för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="d7764-113">Specifies the backup storage redundancy type.</span></span>

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

### <span data-ttu-id="d7764-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7764-114">-DefaultProfile</span></span>
<span data-ttu-id="d7764-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7764-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7764-116">-Valv</span><span class="sxs-lookup"><span data-stu-id="d7764-116">-Vault</span></span>
<span data-ttu-id="d7764-117">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="d7764-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="d7764-118">Valvet måste vara ett **AzureRmRecoveryServicesVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d7764-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="d7764-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d7764-119">-Confirm</span></span>
<span data-ttu-id="d7764-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d7764-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7764-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7764-121">-WhatIf</span></span>
<span data-ttu-id="d7764-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d7764-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7764-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d7764-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7764-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7764-124">CommonParameters</span></span>
<span data-ttu-id="d7764-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7764-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7764-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7764-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7764-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7764-127">INPUTS</span></span>

### <span data-ttu-id="d7764-128">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d7764-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="d7764-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7764-129">OUTPUTS</span></span>

### <span data-ttu-id="d7764-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="d7764-130">System.Void</span></span>

## <span data-ttu-id="d7764-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7764-131">NOTES</span></span>

## <span data-ttu-id="d7764-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7764-132">RELATED LINKS</span></span>

[<span data-ttu-id="d7764-133">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="d7764-133">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="d7764-134">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d7764-134">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


