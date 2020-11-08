---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 56C7B6F5-C2AC-4C5A-8930-645374694CC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 053bb1bfb31b90a91d69e50b77ac6411321014f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099020"
---
# <span data-ttu-id="49011-101">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="49011-101">Set-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="49011-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49011-102">SYNOPSIS</span></span>
<span data-ttu-id="49011-103">Anger Azure SQL Server-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="49011-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="49011-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49011-104">SYNTAX</span></span>

### <span data-ttu-id="49011-105">EnableSqlServerExtension (standard)</span><span class="sxs-lookup"><span data-stu-id="49011-105">EnableSqlServerExtension (Default)</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>]
 [[-AutoPatchingSettings] <AutoPatchingSettings>] [[-AutoBackupSettings] <AutoBackupSettings>]
 [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="49011-106">DisableSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="49011-106">DisableSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="49011-107">UninstallSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="49011-107">UninstallSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="49011-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49011-108">DESCRIPTION</span></span>
<span data-ttu-id="49011-109">Cmdleten **set-AzureVMSqlServerExtension** anger tillägget för Azure SQL-servern på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="49011-109">The **Set-AzureVMSqlServerExtension** cmdlet sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="49011-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49011-110">EXAMPLES</span></span>

### <span data-ttu-id="49011-111">Exempel 1: Ange inställningar för automatisk uppdatering på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="49011-111">Example 1: Set auto-patching settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoPatchingSettings $APS | Update-AzureVM
```

<span data-ttu-id="49011-112">Det här kommandot anger inställningar för automatisk uppdatering på en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="49011-112">This command sets auto-patching settings on an Azure virtual machine.</span></span>

### <span data-ttu-id="49011-113">Exempel 2: Ange inställningar för automatisk säkerhets kopiering på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="49011-113">Example 2: Set auto-backup settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoBackupSettings $ABS | Update-AzureVM
```

<span data-ttu-id="49011-114">Det här kommandot ställer in inställningar för automatisk säkerhets kopiering på den virtuella Azure-datorn.</span><span class="sxs-lookup"><span data-stu-id="49011-114">This command sets auto-backup settings on Azure virtual machine.</span></span>

### <span data-ttu-id="49011-115">Exempel 3: inaktivera ett SQL Server-tillägg på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="49011-115">Example 3: Disable an SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Disable
```

<span data-ttu-id="49011-116">Det här kommandot inaktiverar tillägget för SQL Server på en given virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="49011-116">This command disables SQL Server virtual machine extension on a given virtual machine.</span></span>

### <span data-ttu-id="49011-117">Exempel 4: Avinstallera ett SQL Server-tillägg på en specifik virtuell dator</span><span class="sxs-lookup"><span data-stu-id="49011-117">Example 4: Uninstall an SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Uninstall
```

<span data-ttu-id="49011-118">Det här kommandot avinstallerar ett virtuellt dator tillägg för SQL Server på den virtuella datorn med namnet VMName.</span><span class="sxs-lookup"><span data-stu-id="49011-118">This command uninstalls a SQL Server virtual machine extension on the virtual machine named VMName.</span></span>

## <span data-ttu-id="49011-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49011-119">PARAMETERS</span></span>

### <span data-ttu-id="49011-120">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="49011-120">-AutoBackupSettings</span></span>
<span data-ttu-id="49011-121">Anger automatisk säkerhets kopiering för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="49011-121">Specifies the automatic SQL Server backup settings.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49011-122">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="49011-122">-AutoPatchingSettings</span></span>
<span data-ttu-id="49011-123">Anger automatiska inställningar för uppdatering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="49011-123">Specifies the automatic SQL Server patching settings.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49011-124">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="49011-124">-Disable</span></span>
<span data-ttu-id="49011-125">Anger att denna cmdlet inaktiverar tillägget.</span><span class="sxs-lookup"><span data-stu-id="49011-125">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49011-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="49011-126">-InformationAction</span></span>
<span data-ttu-id="49011-127">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="49011-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="49011-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="49011-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49011-129">Vidare</span><span class="sxs-lookup"><span data-stu-id="49011-129">Continue</span></span>
- <span data-ttu-id="49011-130">Över</span><span class="sxs-lookup"><span data-stu-id="49011-130">Ignore</span></span>
- <span data-ttu-id="49011-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="49011-131">Inquire</span></span>
- <span data-ttu-id="49011-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="49011-132">SilentlyContinue</span></span>
- <span data-ttu-id="49011-133">Stanna</span><span class="sxs-lookup"><span data-stu-id="49011-133">Stop</span></span>
- <span data-ttu-id="49011-134">Avbryt</span><span class="sxs-lookup"><span data-stu-id="49011-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49011-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="49011-135">-InformationVariable</span></span>
<span data-ttu-id="49011-136">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="49011-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49011-137">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="49011-137">-KeyVaultCredentialSettings</span></span>
<span data-ttu-id="49011-138">Anger inställningar för autentiseringsuppgifter för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="49011-138">Specifies key vault credential settings.</span></span>

```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49011-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="49011-139">-Profile</span></span>
<span data-ttu-id="49011-140">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="49011-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49011-141">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="49011-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49011-142">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="49011-142">-ReferenceName</span></span>
<span data-ttu-id="49011-143">Anger referens namnet på SQL Server-tillägget.</span><span class="sxs-lookup"><span data-stu-id="49011-143">Specifies the reference name of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49011-144">-Avinstallera</span><span class="sxs-lookup"><span data-stu-id="49011-144">-Uninstall</span></span>
<span data-ttu-id="49011-145">Anger att denna cmdlet avinstallerar SQL Server-tillägget från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="49011-145">Indicates that this cmdlet uninstalls the SQL Server extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49011-146">-Version</span><span class="sxs-lookup"><span data-stu-id="49011-146">-Version</span></span>
<span data-ttu-id="49011-147">Anger vilken version av SQL Server-tillägget som Get-AzureVMSqlServerExtension hämtar inställningar från.</span><span class="sxs-lookup"><span data-stu-id="49011-147">Specifies the version of the SQL Server extension that Get-AzureVMSqlServerExtension retrieves settings from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49011-148">-VM</span><span class="sxs-lookup"><span data-stu-id="49011-148">-VM</span></span>
<span data-ttu-id="49011-149">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="49011-149">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49011-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49011-150">CommonParameters</span></span>
<span data-ttu-id="49011-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49011-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49011-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49011-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49011-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49011-153">INPUTS</span></span>

## <span data-ttu-id="49011-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49011-154">OUTPUTS</span></span>

## <span data-ttu-id="49011-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49011-155">NOTES</span></span>

## <span data-ttu-id="49011-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49011-156">RELATED LINKS</span></span>

[<span data-ttu-id="49011-157">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="49011-157">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="49011-158">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="49011-158">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)


