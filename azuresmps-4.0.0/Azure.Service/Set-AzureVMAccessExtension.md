---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8F881112-3603-4EE7-88A4-ED45040A60AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc71708c0dff8e359813bb01db0f09f2c91a0cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099041"
---
# <span data-ttu-id="22b5f-101">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="22b5f-101">Set-AzureVMAccessExtension</span></span>

## <span data-ttu-id="22b5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="22b5f-103">Anger VMAccess-tillägget för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="22b5f-103">Sets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="22b5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22b5f-104">SYNTAX</span></span>

### <span data-ttu-id="22b5f-105">EnableAccessExtension (standard)</span><span class="sxs-lookup"><span data-stu-id="22b5f-105">EnableAccessExtension (Default)</span></span>
```
Set-AzureVMAccessExtension [[-UserName] <String>] [[-Password] <String>] [[-ReferenceName] <String>]
 [[-Version] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="22b5f-106">DisableAccessExtension</span><span class="sxs-lookup"><span data-stu-id="22b5f-106">DisableAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="22b5f-107">UninstallAccessExtension</span><span class="sxs-lookup"><span data-stu-id="22b5f-107">UninstallAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="22b5f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22b5f-108">DESCRIPTION</span></span>
<span data-ttu-id="22b5f-109">Cmdleten **set-AzureVMAccessExtension** lägger till VMAccess-tillägget för virtuell dator till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="22b5f-109">The **Set-AzureVMAccessExtension** cmdlet adds the Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="22b5f-110">VMAccess-tillägget kan användas för att ange ett tillfälligt lösen ord och det bör ändras direkt efter att du har loggat in på datorn.</span><span class="sxs-lookup"><span data-stu-id="22b5f-110">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="22b5f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22b5f-111">EXAMPLES</span></span>

### <span data-ttu-id="22b5f-112">Exempel 1: Ange tillägget VMAccess som används för en viss virtuell dator</span><span class="sxs-lookup"><span data-stu-id="22b5f-112">Example 1: Set the VMAccess extension applied to a specified virtual machine</span></span>
```
PS C:\> Set-AzureVMAccessExtension -VM $VM -UserName $User -Password $PWD;
```

<span data-ttu-id="22b5f-113">Det här kommandot anger det VMAccess-tillägg som används för den angivna virtuella datorn enligt variabel $VM.</span><span class="sxs-lookup"><span data-stu-id="22b5f-113">This command sets the VMAccess extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="22b5f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22b5f-114">PARAMETERS</span></span>

### <span data-ttu-id="22b5f-115">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="22b5f-115">-Disable</span></span>
<span data-ttu-id="22b5f-116">Anger att den här cmdleten ställer in det tilläggs tillstånd som ska inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="22b5f-116">Indicates that this cmdlet sets the Extension State to Disable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b5f-117">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="22b5f-117">-ForceUpdate</span></span>
<span data-ttu-id="22b5f-118">Anger att denna cmdlet Återtillämpar en konfiguration för ett tillägg när konfigurationen inte har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="22b5f-118">Indicates that this cmdlet reapplies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22b5f-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="22b5f-119">-InformationAction</span></span>
<span data-ttu-id="22b5f-120">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="22b5f-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="22b5f-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="22b5f-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22b5f-122">Vidare</span><span class="sxs-lookup"><span data-stu-id="22b5f-122">Continue</span></span>
- <span data-ttu-id="22b5f-123">Över</span><span class="sxs-lookup"><span data-stu-id="22b5f-123">Ignore</span></span>
- <span data-ttu-id="22b5f-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="22b5f-124">Inquire</span></span>
- <span data-ttu-id="22b5f-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="22b5f-125">SilentlyContinue</span></span>
- <span data-ttu-id="22b5f-126">Stanna</span><span class="sxs-lookup"><span data-stu-id="22b5f-126">Stop</span></span>
- <span data-ttu-id="22b5f-127">Avbryt</span><span class="sxs-lookup"><span data-stu-id="22b5f-127">Suspend</span></span>

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

### <span data-ttu-id="22b5f-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="22b5f-128">-InformationVariable</span></span>
<span data-ttu-id="22b5f-129">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="22b5f-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="22b5f-130">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="22b5f-130">-Password</span></span>
<span data-ttu-id="22b5f-131">Anger lösen ordet för att återställa den virtuella datorns autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="22b5f-131">Specifies the password for resetting the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b5f-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="22b5f-132">-Profile</span></span>
<span data-ttu-id="22b5f-133">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="22b5f-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="22b5f-134">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="22b5f-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="22b5f-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="22b5f-135">-ReferenceName</span></span>
<span data-ttu-id="22b5f-136">Anger referens namnet för Access-tillägget.</span><span class="sxs-lookup"><span data-stu-id="22b5f-136">Specifies the reference name of the access extension.</span></span>

<span data-ttu-id="22b5f-137">Det här är en användardefinierad sträng som används för att referera till ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="22b5f-137">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="22b5f-138">Det anges när tillägget läggs till på den virtuella datorn för första gången.</span><span class="sxs-lookup"><span data-stu-id="22b5f-138">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="22b5f-139">För kommande uppdateringar ska du ange det tidigare använda referens namnet när du uppdaterar tillägget.</span><span class="sxs-lookup"><span data-stu-id="22b5f-139">For subsequent updates, you should specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="22b5f-140">*ReferenceName* som tilldelats till ett tillägg returneras med cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="22b5f-140">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b5f-141">-Avinstallera</span><span class="sxs-lookup"><span data-stu-id="22b5f-141">-Uninstall</span></span>
<span data-ttu-id="22b5f-142">Anger om den här cmdleten avinstallerar åtkomst tillägget.</span><span class="sxs-lookup"><span data-stu-id="22b5f-142">Indicates whether this cmdlet uninstalls the access extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b5f-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="22b5f-143">-UserName</span></span>
<span data-ttu-id="22b5f-144">Anger det användar namn som används i denna cmdlet för att återställa den virtuella datorns autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="22b5f-144">Specifies the user name that this cmdlet uses to reset the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b5f-145">-Version</span><span class="sxs-lookup"><span data-stu-id="22b5f-145">-Version</span></span>
<span data-ttu-id="22b5f-146">Anger version för tillägget.</span><span class="sxs-lookup"><span data-stu-id="22b5f-146">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="22b5f-147">-VM</span><span class="sxs-lookup"><span data-stu-id="22b5f-147">-VM</span></span>
<span data-ttu-id="22b5f-148">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="22b5f-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="22b5f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b5f-149">CommonParameters</span></span>
<span data-ttu-id="22b5f-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b5f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b5f-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b5f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b5f-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22b5f-152">INPUTS</span></span>

## <span data-ttu-id="22b5f-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22b5f-153">OUTPUTS</span></span>

## <span data-ttu-id="22b5f-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22b5f-154">NOTES</span></span>

## <span data-ttu-id="22b5f-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22b5f-155">RELATED LINKS</span></span>

[<span data-ttu-id="22b5f-156">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="22b5f-156">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="22b5f-157">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="22b5f-157">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)


