---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 0da09971892c03c157d9679da8feb88bdd66a73f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089336"
---
# <span data-ttu-id="e88c1-101">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e88c1-101">Unregister-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="e88c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e88c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e88c1-103">Avregistrerar en Windows-Server eller annan behållare från valvet.</span><span class="sxs-lookup"><span data-stu-id="e88c1-103">Unregisters a Windows Server or other container from the vault.</span></span>

## <span data-ttu-id="e88c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e88c1-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e88c1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e88c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e88c1-106">Med cmdleten **Unregistered-AzRecoveryServicesBackupContainer** avregistrerar du en Windows Server eller annan säkerhets kopierings behållare från valvet.</span><span class="sxs-lookup"><span data-stu-id="e88c1-106">The **Unregister-AzRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="e88c1-107">Denna cmdlet tar bort referenser till en behållare från valvet.</span><span class="sxs-lookup"><span data-stu-id="e88c1-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="e88c1-108">Innan du kan avregistrera en behållare måste du ta bort alla skyddade data som är kopplade till den behållaren.</span><span class="sxs-lookup"><span data-stu-id="e88c1-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="e88c1-109">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e88c1-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e88c1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e88c1-110">EXAMPLES</span></span>

### <span data-ttu-id="e88c1-111">Exempel 1: avregistrera en Windows Server från valvet</span><span class="sxs-lookup"><span data-stu-id="e88c1-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="e88c1-112">Det första kommandot hämtar Windows-behållaren med namnet server01.contoso.com som är registrerad i valvet och lagrar det sedan i $Cont variabel.</span><span class="sxs-lookup"><span data-stu-id="e88c1-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>
<span data-ttu-id="e88c1-113">Det andra kommandot avregistrerar den angivna Windows-servern från Azure Backup-valvet.</span><span class="sxs-lookup"><span data-stu-id="e88c1-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="e88c1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e88c1-114">PARAMETERS</span></span>

### <span data-ttu-id="e88c1-115">-Container</span><span class="sxs-lookup"><span data-stu-id="e88c1-115">-Container</span></span>
<span data-ttu-id="e88c1-116">Anger ett säkerhets kopierings objekt som ska avregistreras.</span><span class="sxs-lookup"><span data-stu-id="e88c1-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="e88c1-117">För att hämta ett **BackupContainer** -objekt, Använd cmdleten Get-AzRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="e88c1-117">To obtain a **BackupContainer** object, use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e88c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88c1-118">-DefaultProfile</span></span>
<span data-ttu-id="e88c1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e88c1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e88c1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e88c1-120">-PassThru</span></span>
<span data-ttu-id="e88c1-121">Returnera behållaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e88c1-121">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="e88c1-122">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e88c1-122">-VaultId</span></span>
<span data-ttu-id="e88c1-123">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="e88c1-123">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e88c1-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e88c1-124">-Confirm</span></span>
<span data-ttu-id="e88c1-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e88c1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e88c1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88c1-126">-WhatIf</span></span>
<span data-ttu-id="e88c1-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e88c1-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e88c1-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e88c1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e88c1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88c1-129">CommonParameters</span></span>
<span data-ttu-id="e88c1-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e88c1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88c1-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e88c1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88c1-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e88c1-132">INPUTS</span></span>

### <span data-ttu-id="e88c1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e88c1-133">System.String</span></span>

## <span data-ttu-id="e88c1-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e88c1-134">OUTPUTS</span></span>

### <span data-ttu-id="e88c1-135">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="e88c1-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="e88c1-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e88c1-136">NOTES</span></span>

## <span data-ttu-id="e88c1-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e88c1-137">RELATED LINKS</span></span>

[<span data-ttu-id="e88c1-138">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e88c1-138">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)


