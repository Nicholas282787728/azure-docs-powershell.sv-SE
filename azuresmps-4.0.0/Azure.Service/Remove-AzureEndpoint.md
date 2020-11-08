---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5A068EC9-3745-4219-BA03-C56CB9D9D157
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24fad9fc499c3f7abec5e7539fd1e221835849ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099708"
---
# <span data-ttu-id="4698a-101">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="4698a-101">Remove-AzureEndpoint</span></span>

## <span data-ttu-id="4698a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4698a-102">SYNOPSIS</span></span>
<span data-ttu-id="4698a-103">Tar bort en slut punkt från en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="4698a-103">Deletes an endpoint from an Azure virtual machine.</span></span>

## <span data-ttu-id="4698a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4698a-104">SYNTAX</span></span>

```
Remove-AzureEndpoint [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4698a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4698a-105">DESCRIPTION</span></span>
<span data-ttu-id="4698a-106">Cmdleten **Remove-AzureEndpoint** tar bort en slut punkt från ett objekt i Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="4698a-106">The **Remove-AzureEndpoint** cmdlet deletes an endpoint from an Azure virtual machine object.</span></span>

## <span data-ttu-id="4698a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4698a-107">EXAMPLES</span></span>

### <span data-ttu-id="4698a-108">Exempel 1: ta bort en slut punkt</span><span class="sxs-lookup"><span data-stu-id="4698a-108">Example 1: Remove an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine01" | Remove-AzureEndpoint -Name "HttpIn" | Update-AzureVM
```

<span data-ttu-id="4698a-109">Det här kommandot hämtar konfigurationen för en virtuell dator med namnet VirtualMachine01 med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="4698a-109">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="4698a-110">Kommandot skickar det till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="4698a-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4698a-111">Denna cmdlet tar bort en slut punkt som heter Httpin.</span><span class="sxs-lookup"><span data-stu-id="4698a-111">This cmdlet removes an endpoint named HttpIn.</span></span>
<span data-ttu-id="4698a-112">Kommandot skickar det virtuella datorobjektet till cmdleten **Update-AzureVM** som implementerar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="4698a-112">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="4698a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4698a-113">PARAMETERS</span></span>

### <span data-ttu-id="4698a-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4698a-114">-InformationAction</span></span>
<span data-ttu-id="4698a-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="4698a-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4698a-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4698a-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4698a-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="4698a-117">Continue</span></span>
- <span data-ttu-id="4698a-118">Över</span><span class="sxs-lookup"><span data-stu-id="4698a-118">Ignore</span></span>
- <span data-ttu-id="4698a-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="4698a-119">Inquire</span></span>
- <span data-ttu-id="4698a-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4698a-120">SilentlyContinue</span></span>
- <span data-ttu-id="4698a-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="4698a-121">Stop</span></span>
- <span data-ttu-id="4698a-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="4698a-122">Suspend</span></span>

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

### <span data-ttu-id="4698a-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4698a-123">-InformationVariable</span></span>
<span data-ttu-id="4698a-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="4698a-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4698a-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="4698a-125">-Name</span></span>
<span data-ttu-id="4698a-126">Anger namnet på den slut punkt som denna cmdlet tar bort från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4698a-126">Specifies the name of the endpoint that this cmdlet deletes from the virtual machine.</span></span>

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

### <span data-ttu-id="4698a-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="4698a-127">-Profile</span></span>
<span data-ttu-id="4698a-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4698a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4698a-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4698a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4698a-130">-VM</span><span class="sxs-lookup"><span data-stu-id="4698a-130">-VM</span></span>
<span data-ttu-id="4698a-131">Anger den virtuella dator som den här cmdleten tar bort en slut punkt från.</span><span class="sxs-lookup"><span data-stu-id="4698a-131">Specifies the virtual machine from which this cmdlet deletes an endpoint.</span></span>

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

### <span data-ttu-id="4698a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4698a-132">CommonParameters</span></span>
<span data-ttu-id="4698a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4698a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4698a-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4698a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4698a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4698a-135">INPUTS</span></span>

## <span data-ttu-id="4698a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4698a-136">OUTPUTS</span></span>

## <span data-ttu-id="4698a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4698a-137">NOTES</span></span>

## <span data-ttu-id="4698a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4698a-138">RELATED LINKS</span></span>

[<span data-ttu-id="4698a-139">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="4698a-139">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="4698a-140">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="4698a-140">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="4698a-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4698a-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="4698a-142">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="4698a-142">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="4698a-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4698a-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


