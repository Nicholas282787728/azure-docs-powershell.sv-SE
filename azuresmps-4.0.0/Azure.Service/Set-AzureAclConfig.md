---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099662"
---
# <span data-ttu-id="ab3f7-101">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="ab3f7-101">Set-AzureAclConfig</span></span>

## <span data-ttu-id="ab3f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3f7-103">Ändrar ett konfigurations objekt för ACL.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-103">Modifies an ACL configuration object.</span></span>

## <span data-ttu-id="ab3f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab3f7-104">SYNTAX</span></span>

### <span data-ttu-id="ab3f7-105">AddRule</span><span class="sxs-lookup"><span data-stu-id="ab3f7-105">AddRule</span></span>
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ab3f7-106">RemoveRule</span><span class="sxs-lookup"><span data-stu-id="ab3f7-106">RemoveRule</span></span>
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ab3f7-107">SetRule</span><span class="sxs-lookup"><span data-stu-id="ab3f7-107">SetRule</span></span>
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ab3f7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab3f7-108">DESCRIPTION</span></span>
<span data-ttu-id="ab3f7-109">Cmdleten **set-AzureAclConfig** ändrar en ACL-konfigurations objekt från en befintlig Azure Virtual Machine-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-109">The **Set-AzureAclConfig** cmdlet modifies an access control list (ACL) configuration object from an existing Azure virtual machine configuration.</span></span>

## <span data-ttu-id="ab3f7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab3f7-110">EXAMPLES</span></span>

### <span data-ttu-id="ab3f7-111">Exempel 1: lägga till en regel i en ny ACL-konfiguration</span><span class="sxs-lookup"><span data-stu-id="ab3f7-111">Example 1: Add a rule to a new ACL configuration</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

<span data-ttu-id="ab3f7-112">Det första kommandot skapar en ACL-konfiguration och lagrar den sedan i $Acl variabel.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-112">The first command creates an ACL configuration, and then stores it in the $Acl variable.</span></span>

<span data-ttu-id="ab3f7-113">Det andra kommandot lägger till en ny regel i konfigurationen som lagras i $Acl.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-113">The second command adds a new rule to the configuration stored in $Acl.</span></span>
<span data-ttu-id="ab3f7-114">Kommandot anger en åtgärd, ett undernät, en order och en beskrivning av regeln.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-114">The command specifies an action, subnet, order, and description for the rule.</span></span>

### <span data-ttu-id="ab3f7-115">Exempel 2: ändra en regel i en ACL-konfiguration</span><span class="sxs-lookup"><span data-stu-id="ab3f7-115">Example 2: Modify a rule in an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="ab3f7-116">Det första kommandot får den virtuella datorn som heter VirtualMachine07 i tjänsten ContosoService med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ab3f7-116">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ab3f7-117">Kommandot skickar det objektet till cmdleten **Get-AzureAclConfig** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-117">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ab3f7-118">Denna cmdlet hämtar ACL-konfigurationen för slut punkten med namnet Web.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-118">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="ab3f7-119">Kommandot lagrar ACL-konfigurationsobjekt i $Acl variabel.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-119">The command stores that ACL configuration object in the $Acl variable.</span></span>

<span data-ttu-id="ab3f7-120">Det andra kommandot ändrar regeln som har ID 0 för.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-120">The second command modifies the rule that has the ID of 0.</span></span>
<span data-ttu-id="ab3f7-121">Kommandot ändrar ordningen och beskrivningen av regeln.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-121">The command changes the order and the description of the rule.</span></span>

<span data-ttu-id="ab3f7-122">Kommandot Final anger ACL-konfigurationsobjektet för den virtuella datorn med cmdleten **set-AzureEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="ab3f7-122">The final command sets the ACL configuration object for that virtual machine by using the **Set-AzureEndpoint** cmdlet.</span></span>
<span data-ttu-id="ab3f7-123">Kommandot uppdaterar också den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-123">The command also updates that virtual machine.</span></span>

### <span data-ttu-id="ab3f7-124">Exempel 3: ta bort en regel från en ACL-konfiguration</span><span class="sxs-lookup"><span data-stu-id="ab3f7-124">Example 3: Remove a rule from an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="ab3f7-125">Det första kommandot lagrar ett ACL-konfigurationsobjekt i $Acl variabel.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-125">The first command stores an ACL configuration object in the $Acl variable.</span></span>
<span data-ttu-id="ab3f7-126">Det här är samma som i föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-126">This is the same as the previous example.</span></span>

<span data-ttu-id="ab3f7-127">Det andra kommandot tar bort regeln med ID 0 från ACL-konfigurationen i $Acl.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-127">The second command removes the rule that has the ID 0 from the ACL configuration in $Acl.</span></span>

<span data-ttu-id="ab3f7-128">Kommandot Final anger ACL-konfigurationsobjekt för den virtuella datorn och uppdaterar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-128">The final command sets the ACL configuration object for the virtual machine and updates that virtual machine.</span></span>
<span data-ttu-id="ab3f7-129">Det här är samma som i föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-129">This is the same as the previous example.</span></span>

## <span data-ttu-id="ab3f7-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab3f7-130">PARAMETERS</span></span>

### <span data-ttu-id="ab3f7-131">-ACL</span><span class="sxs-lookup"><span data-stu-id="ab3f7-131">-ACL</span></span>
<span data-ttu-id="ab3f7-132">Anger ett ACL-konfigurationsobjekt som ska ändras av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-132">Specifies an ACL configuration object that this cmdlet modifies.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f7-133">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="ab3f7-133">-Action</span></span>
<span data-ttu-id="ab3f7-134">Anger åtgärd för den regel som denna cmdlet lägger till eller ändrar.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-134">Specifies the action for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="ab3f7-135">Giltiga värden är: Permit och Deny.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-135">Valid values are: Permit and Deny.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f7-136">-AddRule</span><span class="sxs-lookup"><span data-stu-id="ab3f7-136">-AddRule</span></span>
<span data-ttu-id="ab3f7-137">Anger att denna cmdlet lägger till en regel i ACL-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-137">Indicates that this cmdlet adds a rule to the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f7-138">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ab3f7-138">-Description</span></span>
<span data-ttu-id="ab3f7-139">Anger en beskrivning för den regel som denna cmdlet lägger till eller ändrar.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-139">Specifies a description for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f7-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ab3f7-140">-InformationAction</span></span>
<span data-ttu-id="ab3f7-141">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ab3f7-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ab3f7-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ab3f7-143">Vidare</span><span class="sxs-lookup"><span data-stu-id="ab3f7-143">Continue</span></span>
- <span data-ttu-id="ab3f7-144">Över</span><span class="sxs-lookup"><span data-stu-id="ab3f7-144">Ignore</span></span>
- <span data-ttu-id="ab3f7-145">Inquire</span><span class="sxs-lookup"><span data-stu-id="ab3f7-145">Inquire</span></span>
- <span data-ttu-id="ab3f7-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ab3f7-146">SilentlyContinue</span></span>
- <span data-ttu-id="ab3f7-147">Stanna</span><span class="sxs-lookup"><span data-stu-id="ab3f7-147">Stop</span></span>
- <span data-ttu-id="ab3f7-148">Avbryt</span><span class="sxs-lookup"><span data-stu-id="ab3f7-148">Suspend</span></span>

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

### <span data-ttu-id="ab3f7-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ab3f7-149">-InformationVariable</span></span>
<span data-ttu-id="ab3f7-150">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-150">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ab3f7-151">-Beställ</span><span class="sxs-lookup"><span data-stu-id="ab3f7-151">-Order</span></span>
<span data-ttu-id="ab3f7-152">Anger bearbetnings ordningen för den regel som denna cmdlet lägger till eller ändrar.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-152">Specifies the processing order for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f7-153">-RemoteSubnet</span><span class="sxs-lookup"><span data-stu-id="ab3f7-153">-RemoteSubnet</span></span>
<span data-ttu-id="ab3f7-154">Anger fjärrundernät för den regel som denna cmdlet lägger till eller ändrar.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-154">Specifies the remote subnet for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="ab3f7-155">Anger en adress i CIDR-format (Classless Interdomain Routing).</span><span class="sxs-lookup"><span data-stu-id="ab3f7-155">Specifies an address in Classless Interdomain Routing (CIDR) format.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f7-156">-RemoveRule</span><span class="sxs-lookup"><span data-stu-id="ab3f7-156">-RemoveRule</span></span>
<span data-ttu-id="ab3f7-157">Anger att denna cmdlet tar bort en regel från ACL-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-157">Indicates that this cmdlet removes a rule from the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f7-158">-RuleId</span><span class="sxs-lookup"><span data-stu-id="ab3f7-158">-RuleId</span></span>
<span data-ttu-id="ab3f7-159">Anger ID för den regel som denna cmdlet tar bort eller ändrar för ACL-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-159">Specifies the ID of the rule that this cmdlet removes or modifies for the ACL configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f7-160">-SetRule</span><span class="sxs-lookup"><span data-stu-id="ab3f7-160">-SetRule</span></span>
<span data-ttu-id="ab3f7-161">Anger att denna cmdlet ändrar en regel i ACL-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-161">Indicates that this cmdlet modifies a rule in the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f7-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3f7-162">CommonParameters</span></span>
<span data-ttu-id="ab3f7-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab3f7-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3f7-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab3f7-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3f7-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab3f7-165">INPUTS</span></span>

## <span data-ttu-id="ab3f7-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab3f7-166">OUTPUTS</span></span>

## <span data-ttu-id="ab3f7-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab3f7-167">NOTES</span></span>

## <span data-ttu-id="ab3f7-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab3f7-168">RELATED LINKS</span></span>

[<span data-ttu-id="ab3f7-169">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="ab3f7-169">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="ab3f7-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ab3f7-170">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ab3f7-171">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="ab3f7-171">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="ab3f7-172">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="ab3f7-172">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="ab3f7-173">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab3f7-173">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="ab3f7-174">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ab3f7-174">Update-AzureVM</span></span>](./Update-AzureVM.md)


