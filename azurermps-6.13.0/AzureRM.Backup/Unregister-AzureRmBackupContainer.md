---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/unregister-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 8c90137e142086d7ea7c0bcc34321b3f38a12d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575328"
---
# <span data-ttu-id="2516f-101">Unregister-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2516f-101">Unregister-AzureRmBackupContainer</span></span>

## <span data-ttu-id="2516f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2516f-102">SYNOPSIS</span></span>
<span data-ttu-id="2516f-103">Avregistrerar en behållare från ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="2516f-103">Unregisters a container from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2516f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2516f-104">SYNTAX</span></span>

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2516f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2516f-105">DESCRIPTION</span></span>
<span data-ttu-id="2516f-106">Med cmdleten **Unregistered-AzureRmBackupContainer** avregistrerar du den virtuella Windows-servern eller Azure-datorn från ett Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="2516f-106">The **Unregister-AzureRmBackupContainer** cmdlet unregisters the Windows Server or Azure virtual machine from an Azure Backup vault.</span></span>
<span data-ttu-id="2516f-107">Denna cmdlet tar bort referenser till en behållare från säkerhets kopierings valvet.</span><span class="sxs-lookup"><span data-stu-id="2516f-107">This cmdlet removes references to a container from the Backup vault.</span></span>
<span data-ttu-id="2516f-108">Innan du kan avregistrera en behållare måste du ta bort alla skyddade data som är kopplade till den behållaren.</span><span class="sxs-lookup"><span data-stu-id="2516f-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

## <span data-ttu-id="2516f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2516f-109">EXAMPLES</span></span>

### <span data-ttu-id="2516f-110">Exempel 1: avregistrera en Windows Server</span><span class="sxs-lookup"><span data-stu-id="2516f-110">Example 1: Unregister a Windows Server</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

<span data-ttu-id="2516f-111">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2516f-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="2516f-112">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="2516f-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="2516f-113">Det andra kommandot får en behållare som har det angivna namnet i valvet i $Vault genom att använda Get-AzureRmBackupContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2516f-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="2516f-114">Kommandot lagrar objektet i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="2516f-114">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="2516f-115">Det sista kommandot avregistrerar den angivna Windows-servern från Azure Backup-valvet.</span><span class="sxs-lookup"><span data-stu-id="2516f-115">The final command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="2516f-116">Exempel 2: avregistrera en Windows Server utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="2516f-116">Example 2: Unregister a Windows Server without confirmation</span></span>
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

<span data-ttu-id="2516f-117">Det här kommandot avregistrerar den angivna Windows-servern från Azure Backup-valvet, på samma sätt som i det första exemplet.</span><span class="sxs-lookup"><span data-stu-id="2516f-117">This command unregisters the specified Windows Server from the Azure Backup vault, just as in the first example.</span></span>
<span data-ttu-id="2516f-118">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="2516f-118">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2516f-119">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2516f-119">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2516f-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2516f-120">PARAMETERS</span></span>

### <span data-ttu-id="2516f-121">-Container</span><span class="sxs-lookup"><span data-stu-id="2516f-121">-Container</span></span>
<span data-ttu-id="2516f-122">Anger den virtuella Windows Server-eller Azure-dator som denna cmdlet avregistrerar.</span><span class="sxs-lookup"><span data-stu-id="2516f-122">Specifies the Windows Server or Azure virtual machine that this cmdlet unregisters.</span></span>
<span data-ttu-id="2516f-123">För att få en **AzureRmBackupContainer** , Använd cmdleten Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="2516f-123">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2516f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2516f-124">-DefaultProfile</span></span>
<span data-ttu-id="2516f-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2516f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2516f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="2516f-126">-Force</span></span>
<span data-ttu-id="2516f-127">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2516f-127">Forces the command to run without asking for user confirmation.</span></span>
<span data-ttu-id="2516f-128">Den här parametern är endast relevant för **AzureBackupContainer** -objekt i Windows.</span><span class="sxs-lookup"><span data-stu-id="2516f-128">This parameter is relevant only for **AzureBackupContainer** objects of type Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2516f-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2516f-129">-Confirm</span></span>
<span data-ttu-id="2516f-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2516f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2516f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2516f-131">-WhatIf</span></span>
<span data-ttu-id="2516f-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2516f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2516f-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2516f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2516f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2516f-134">CommonParameters</span></span>
<span data-ttu-id="2516f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2516f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2516f-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2516f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2516f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2516f-137">INPUTS</span></span>

### <span data-ttu-id="2516f-138">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2516f-138">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>
<span data-ttu-id="2516f-139">Parametrar: container (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2516f-139">Parameters: Container (ByValue)</span></span>

## <span data-ttu-id="2516f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2516f-140">OUTPUTS</span></span>

### <span data-ttu-id="2516f-141">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="2516f-141">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="2516f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2516f-142">NOTES</span></span>
* <span data-ttu-id="2516f-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="2516f-143">None</span></span>

## <span data-ttu-id="2516f-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2516f-144">RELATED LINKS</span></span>

[<span data-ttu-id="2516f-145">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2516f-145">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="2516f-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="2516f-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="2516f-147">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2516f-147">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


