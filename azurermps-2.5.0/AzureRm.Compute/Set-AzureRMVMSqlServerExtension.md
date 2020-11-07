---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 2a1dbf5eea7f772a7819ed341a681adc24134225
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930305"
---
# <span data-ttu-id="92475-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="92475-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="92475-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92475-102">SYNOPSIS</span></span>
<span data-ttu-id="92475-103">Anger Azure SQL Server-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="92475-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92475-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92475-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92475-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92475-105">DESCRIPTION</span></span>
<span data-ttu-id="92475-106">Cmdleten **set-AzureRmVMSqlServerExtension** anger Server tillägget AzureSQL på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="92475-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="92475-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92475-107">EXAMPLES</span></span>

### <span data-ttu-id="92475-108">Exempel 1: Ange inställningar för automatisk uppdatering på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="92475-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="92475-109">Det första kommandot skapar ett konfigurations objekt med cmdleten **New-AzureVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="92475-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="92475-110">Kommandot lagrar konfigurationen i variabeln $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="92475-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="92475-111">Det andra kommandot får den virtuella datorn med namnet VirtualMachine11 på tjänsten som heter Service02 genom att använda Get-AzureRmVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92475-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="92475-112">Kommandot skickar detta objekt till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="92475-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="92475-113">Den aktuella cmdleten ställer in de automatiska korrigerings inställningarna i $AutoPatchingConfig för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="92475-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="92475-114">Kommandot skickar den virtuella datorn till Update-AzureRmVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92475-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="92475-115">Exempel 2: Ange inställningar för automatisk säkerhets kopiering på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="92475-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="92475-116">Det första kommandot skapar ett konfigurations objekt med cmdleten **New-AzureVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="92475-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="92475-117">Kommandot lagrar konfigurationen i variabeln $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="92475-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="92475-118">Det andra kommandot får den virtuella datorn som heter VirtualMachine11 på tjänsten Service02 och skickar den sedan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92475-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="92475-119">Den aktuella cmdleten ställer in de automatiska säkerhets kopierings inställningarna i $AutoBackupConfig för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="92475-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="92475-120">Kommandot skickar den virtuella datorn till Update-AzureRmVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92475-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="92475-121">Exempel 3: inaktivera ett SQL Server-tillägg på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="92475-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="92475-122">Det här kommandot får en virtuell dator som heter VirtualMachine08 på Service03 och skickar den sedan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92475-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="92475-123">Kommandot inaktiverar tillägget för SQL Server på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="92475-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="92475-124">Exempel 4: Avinstallera ett SQL Server-tillägg på en specifik virtuell dator</span><span class="sxs-lookup"><span data-stu-id="92475-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="92475-125">Det här kommandot får en virtuell dator som heter VirtualMachine08 på Service03 och skickar den sedan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92475-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="92475-126">Kommandot avinstallerar tillägget för en virtuell dator för SQL Server på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="92475-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="92475-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92475-127">PARAMETERS</span></span>

### <span data-ttu-id="92475-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="92475-128">-AutoBackupSettings</span></span>
<span data-ttu-id="92475-129">Anger automatisk säkerhets kopiering för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92475-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="92475-130">Använd New-AzureVMSqlServerAutoBackupConfig cmdlet för att skapa ett **AutoBackupSettings** -objekt.</span><span class="sxs-lookup"><span data-stu-id="92475-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92475-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="92475-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="92475-132">Anger automatiska inställningar för uppdatering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92475-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="92475-133">Använd New-AzureVMSqlServerAutoPatchingConfig cmdlet för att skapa ett **AutoPatchingSettings** -objekt.</span><span class="sxs-lookup"><span data-stu-id="92475-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92475-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92475-134">-DefaultProfile</span></span>
<span data-ttu-id="92475-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92475-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92475-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="92475-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92475-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="92475-137">-Location</span></span>
<span data-ttu-id="92475-138">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="92475-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92475-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="92475-139">-Name</span></span>
<span data-ttu-id="92475-140">Anger namnet på SQL Server-tillägget.</span><span class="sxs-lookup"><span data-stu-id="92475-140">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92475-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92475-141">-ResourceGroupName</span></span>
<span data-ttu-id="92475-142">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="92475-142">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92475-143">-Version</span><span class="sxs-lookup"><span data-stu-id="92475-143">-Version</span></span>
<span data-ttu-id="92475-144">Anger version för SQL Server-tillägget.</span><span class="sxs-lookup"><span data-stu-id="92475-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92475-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="92475-145">-VMName</span></span>
<span data-ttu-id="92475-146">Anger namnet på den virtuella dator där denna cmdlet ställer in SQL Server-tillägget.</span><span class="sxs-lookup"><span data-stu-id="92475-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92475-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92475-147">CommonParameters</span></span>
<span data-ttu-id="92475-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92475-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92475-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92475-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92475-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92475-150">INPUTS</span></span>

### <span data-ttu-id="92475-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="92475-151">None</span></span>
<span data-ttu-id="92475-152">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="92475-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="92475-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92475-153">OUTPUTS</span></span>

### <span data-ttu-id="92475-154">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="92475-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="92475-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92475-155">NOTES</span></span>

## <span data-ttu-id="92475-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92475-156">RELATED LINKS</span></span>

[<span data-ttu-id="92475-157">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92475-157">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="92475-158">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="92475-158">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)





[<span data-ttu-id="92475-159">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="92475-159">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="92475-160">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92475-160">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


