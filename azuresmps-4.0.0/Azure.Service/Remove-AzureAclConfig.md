---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 915CBA29-5A58-4A5D-9F02-976CB76D4800
online version: ''
schema: 2.0.0
ms.openlocfilehash: af98cbdc0be73c87682d0ed004d17cd9e82c9baa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099405"
---
# <span data-ttu-id="c0fb3-101">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c0fb3-101">Remove-AzureAclConfig</span></span>

## <span data-ttu-id="c0fb3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="c0fb3-103">Tar bort ett ACL-konfigurationsobjekt från en konfiguration för en Azure-virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-103">Removes an ACL configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="c0fb3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0fb3-104">SYNTAX</span></span>

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c0fb3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0fb3-105">DESCRIPTION</span></span>
<span data-ttu-id="c0fb3-106">Cmdleten **Remove-AzureAclConfig** tar bort en ACL-konfigurationsfil (Access Control List) från en konfiguration för Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-106">The **Remove-AzureAclConfig** cmdlet removes an access control list (ACL) configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="c0fb3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0fb3-107">EXAMPLES</span></span>

### <span data-ttu-id="c0fb3-108">Exempel 1: ta bort en ACL-konfiguration</span><span class="sxs-lookup"><span data-stu-id="c0fb3-108">Example 1: Remove an ACL configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

<span data-ttu-id="c0fb3-109">Det här kommandot får den virtuella datorn som heter VirtualMachine07 i tjänsten ContosoService med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="c0fb3-109">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="c0fb3-110">Kommandot skickar detta objekt till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c0fb3-111">Denna cmdlet tar bort ACL-konfigurationen för slut punkten som heter Web.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-111">That cmdlet removes the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="c0fb3-112">Kommandot skickar resultatet till cmdleten **Update-AzureVM** , som uppdaterar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-112">The command passes the result to the **Update-AzureVM** cmdlet, which updates the virtual machine.</span></span>

## <span data-ttu-id="c0fb3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0fb3-113">PARAMETERS</span></span>

### <span data-ttu-id="c0fb3-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c0fb3-114">-EndpointName</span></span>
<span data-ttu-id="c0fb3-115">Anger namnet på den slut punkt som den här cmdleten tar bort ACL-konfigurationen från.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-115">Specifies the name of the endpoint from which this cmdlet removes the ACL configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0fb3-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c0fb3-116">-InformationAction</span></span>
<span data-ttu-id="c0fb3-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c0fb3-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c0fb3-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c0fb3-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="c0fb3-119">Continue</span></span>
- <span data-ttu-id="c0fb3-120">Över</span><span class="sxs-lookup"><span data-stu-id="c0fb3-120">Ignore</span></span>
- <span data-ttu-id="c0fb3-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="c0fb3-121">Inquire</span></span>
- <span data-ttu-id="c0fb3-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c0fb3-122">SilentlyContinue</span></span>
- <span data-ttu-id="c0fb3-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="c0fb3-123">Stop</span></span>
- <span data-ttu-id="c0fb3-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c0fb3-124">Suspend</span></span>

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

### <span data-ttu-id="c0fb3-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c0fb3-125">-InformationVariable</span></span>
<span data-ttu-id="c0fb3-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c0fb3-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="c0fb3-127">-Profile</span></span>
<span data-ttu-id="c0fb3-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c0fb3-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c0fb3-130">-VM</span><span class="sxs-lookup"><span data-stu-id="c0fb3-130">-VM</span></span>
<span data-ttu-id="c0fb3-131">Anger den virtuella dator från vilken denna cmdlet tar bort en ACL-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-131">Specifies the virtual machine from which this cmdlet removes an ACL configuration.</span></span>

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

### <span data-ttu-id="c0fb3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0fb3-132">CommonParameters</span></span>
<span data-ttu-id="c0fb3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0fb3-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0fb3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0fb3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0fb3-135">INPUTS</span></span>

## <span data-ttu-id="c0fb3-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0fb3-136">OUTPUTS</span></span>

## <span data-ttu-id="c0fb3-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0fb3-137">NOTES</span></span>

## <span data-ttu-id="c0fb3-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0fb3-138">RELATED LINKS</span></span>

[<span data-ttu-id="c0fb3-139">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c0fb3-139">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="c0fb3-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c0fb3-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="c0fb3-141">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c0fb3-141">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="c0fb3-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c0fb3-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)

[<span data-ttu-id="c0fb3-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c0fb3-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


