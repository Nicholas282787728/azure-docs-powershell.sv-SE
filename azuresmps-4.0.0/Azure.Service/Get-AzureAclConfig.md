---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0A32348E-C38D-4555-8F7C-6515F4EE7F23
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc1c469d35f4cc281fa22252e7e81509be06761
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093399"
---
# <span data-ttu-id="204ed-101">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="204ed-101">Get-AzureAclConfig</span></span>

## <span data-ttu-id="204ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="204ed-102">SYNOPSIS</span></span>
<span data-ttu-id="204ed-103">Hämtar ACL-konfigurationsobjekt från en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="204ed-103">Gets the ACL configuration object from an Azure virtual machine.</span></span>

## <span data-ttu-id="204ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="204ed-104">SYNTAX</span></span>

```
Get-AzureAclConfig [[-EndpointName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="204ed-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="204ed-105">DESCRIPTION</span></span>
<span data-ttu-id="204ed-106">Cmdleten **Get-AzureAclConfig** hämtar ACL-konfigurationsobjektet (Access Control List) från en befintlig virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="204ed-106">The **Get-AzureAclConfig** cmdlet gets the access control list (ACL) configuration object from an existing Azure virtual machine.</span></span>

## <span data-ttu-id="204ed-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="204ed-107">EXAMPLES</span></span>

### <span data-ttu-id="204ed-108">Exempel 1: Hämta ett ACL-konfigurationsobjekt för en virtuell dators slut punkt</span><span class="sxs-lookup"><span data-stu-id="204ed-108">Example 1: Get an ACL configuration object for a virtual machine endpoint</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
```

<span data-ttu-id="204ed-109">Det första kommandot får den virtuella datorn som heter VirtualMachine07 i tjänsten ContosoService med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="204ed-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="204ed-110">Kommandot skickar det objektet till cmdleten **Get-AzureAclConfig** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="204ed-110">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="204ed-111">Denna cmdlet hämtar ACL-konfigurationen för slut punkten med namnet Web.</span><span class="sxs-lookup"><span data-stu-id="204ed-111">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="204ed-112">Kommandot lagrar ACL-konfigurationsobjekt i $Acl variabel.</span><span class="sxs-lookup"><span data-stu-id="204ed-112">The command stores that ACL configuration object in the $Acl variable.</span></span>

## <span data-ttu-id="204ed-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="204ed-113">PARAMETERS</span></span>

### <span data-ttu-id="204ed-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="204ed-114">-EndpointName</span></span>
<span data-ttu-id="204ed-115">Anger namnet på den slut punkt där denna cmdlet hämtar en ACL.</span><span class="sxs-lookup"><span data-stu-id="204ed-115">Specifies the name of the endpoint for which this cmdlet gets an ACL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="204ed-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="204ed-116">-InformationAction</span></span>
<span data-ttu-id="204ed-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="204ed-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="204ed-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="204ed-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="204ed-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="204ed-119">Continue</span></span>
- <span data-ttu-id="204ed-120">Över</span><span class="sxs-lookup"><span data-stu-id="204ed-120">Ignore</span></span>
- <span data-ttu-id="204ed-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="204ed-121">Inquire</span></span>
- <span data-ttu-id="204ed-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="204ed-122">SilentlyContinue</span></span>
- <span data-ttu-id="204ed-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="204ed-123">Stop</span></span>
- <span data-ttu-id="204ed-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="204ed-124">Suspend</span></span>

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

### <span data-ttu-id="204ed-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="204ed-125">-InformationVariable</span></span>
<span data-ttu-id="204ed-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="204ed-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="204ed-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="204ed-127">-Profile</span></span>
<span data-ttu-id="204ed-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="204ed-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="204ed-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="204ed-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="204ed-130">-VM</span><span class="sxs-lookup"><span data-stu-id="204ed-130">-VM</span></span>
<span data-ttu-id="204ed-131">Anger det virtuella dator objekt som den här cmdleten får ACL-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="204ed-131">Specifies the virtual machine object for which this cmdlet gets ACL configuration.</span></span>

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

### <span data-ttu-id="204ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204ed-132">CommonParameters</span></span>
<span data-ttu-id="204ed-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="204ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204ed-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="204ed-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204ed-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="204ed-135">INPUTS</span></span>

## <span data-ttu-id="204ed-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="204ed-136">OUTPUTS</span></span>

## <span data-ttu-id="204ed-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="204ed-137">NOTES</span></span>

## <span data-ttu-id="204ed-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="204ed-138">RELATED LINKS</span></span>

[<span data-ttu-id="204ed-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="204ed-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="204ed-140">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="204ed-140">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="204ed-141">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="204ed-141">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="204ed-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="204ed-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


