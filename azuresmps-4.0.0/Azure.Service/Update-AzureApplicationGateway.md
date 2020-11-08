---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099074"
---
# <span data-ttu-id="7e528-101">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e528-101">Update-AzureApplicationGateway</span></span>

## <span data-ttu-id="7e528-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e528-102">SYNOPSIS</span></span>
<span data-ttu-id="7e528-103">Uppdaterar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7e528-103">Updates an application gateway.</span></span>

## <span data-ttu-id="7e528-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e528-104">SYNTAX</span></span>

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7e528-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e528-105">DESCRIPTION</span></span>
<span data-ttu-id="7e528-106">Cmdleten **Update-AzureApplicationGateway** uppdaterar en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7e528-106">The **Update-AzureApplicationGateway** cmdlet updates an existing application gateway.</span></span>

## <span data-ttu-id="7e528-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e528-107">EXAMPLES</span></span>

### <span data-ttu-id="7e528-108">Exempel 1: ändra en Programgateway genom att använda dess namn</span><span class="sxs-lookup"><span data-stu-id="7e528-108">Example 1: Modify an application gateway by using its name</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

<span data-ttu-id="7e528-109">Det första kommandot stoppar programgatewayen med namnet ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="7e528-109">The first command stops the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="7e528-110">En Programgateway måste stoppas innan du kan ändra virtuella nätverk eller undernät.</span><span class="sxs-lookup"><span data-stu-id="7e528-110">An application gateway must be stopped before you can modify the virtual network or subnets.</span></span>

<span data-ttu-id="7e528-111">Det andra kommandot ändrar det virtuella undernät och undernät för programgatewayen med namnet ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="7e528-111">The second command modifies the virtual subnet and subnets for the application gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="7e528-112">Exempel 2: ändra ytterligare egenskaper för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="7e528-112">Example 2: Modify additional properties of an application gateway</span></span>
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

<span data-ttu-id="7e528-113">Det här kommandot ändrar antalet instanser, Gateway-storlek och beskrivning för den Programgateway som heter ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="7e528-113">This command modifies the instance count, gateway size, and description for the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="7e528-114">Det här kommandot ändrar inte virtuella nätverk eller undernät för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="7e528-114">This command does not modify the virtual network or subnets for the application gateway.</span></span>
<span data-ttu-id="7e528-115">Därför behöver du inte stoppa programgatewayen innan du kör det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="7e528-115">Therefore, you do not have to stop the application gateway before you run this command.</span></span>

### <span data-ttu-id="7e528-116">Exempel 3: ändra en Programgateway genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="7e528-116">Example 3: Modify an application gateway by using the pipeline</span></span>
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

<span data-ttu-id="7e528-117">Det första kommandot hämtar programgatewayen med namnet ApplicationGateway06 med hjälp av cmdleten **Get-AzureApplicationGateway** .</span><span class="sxs-lookup"><span data-stu-id="7e528-117">The first command gets the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGateway** cmdlet.</span></span>
<span data-ttu-id="7e528-118">Kommandot sparar det i $ApplicationGateway variabel.</span><span class="sxs-lookup"><span data-stu-id="7e528-118">The command stores it in the $ApplicationGateway variable.</span></span>

<span data-ttu-id="7e528-119">Det andra kommandot tilldelar värdet medium till egenskapen **GatewaySize** .</span><span class="sxs-lookup"><span data-stu-id="7e528-119">The second command assigns the **GatewaySize** property the value Medium.</span></span>

<span data-ttu-id="7e528-120">Det sista kommandot skickar den uppdaterade $ApplicationGateway till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e528-120">The final command passes the updated $ApplicationGateway to the current cmdlet.</span></span>

## <span data-ttu-id="7e528-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e528-121">PARAMETERS</span></span>

### <span data-ttu-id="7e528-122">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="7e528-122">-Description</span></span>
<span data-ttu-id="7e528-123">Anger en beskrivning av att denna cmdlet tilldelar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="7e528-123">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e528-124">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="7e528-124">-GatewaySize</span></span>
<span data-ttu-id="7e528-125">Anger den storlek som denna cmdlet tilldelar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="7e528-125">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="7e528-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="7e528-126">Valid values are:</span></span>

- <span data-ttu-id="7e528-127">Eld</span><span class="sxs-lookup"><span data-stu-id="7e528-127">Small</span></span>
- <span data-ttu-id="7e528-128">Risk</span><span class="sxs-lookup"><span data-stu-id="7e528-128">Medium</span></span>
- <span data-ttu-id="7e528-129">Höga</span><span class="sxs-lookup"><span data-stu-id="7e528-129">Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e528-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="7e528-130">-InstanceCount</span></span>
<span data-ttu-id="7e528-131">Anger antalet instanser som denna cmdlet tilldelar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="7e528-131">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e528-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e528-132">-Name</span></span>
<span data-ttu-id="7e528-133">Anger namnet på den Application Gateway som uppdateras med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e528-133">Specifies the name of the application gateway that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e528-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="7e528-134">-Profile</span></span>
<span data-ttu-id="7e528-135">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7e528-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7e528-136">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7e528-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e528-137">-Undernät</span><span class="sxs-lookup"><span data-stu-id="7e528-137">-Subnets</span></span>
<span data-ttu-id="7e528-138">Anger en matris med undernät där denna cmdlet distribuerar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="7e528-138">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="7e528-139">Du kan inte uppdatera undernät medan Application Gateway körs.</span><span class="sxs-lookup"><span data-stu-id="7e528-139">You cannot update subnets while the application gateway is running.</span></span>
<span data-ttu-id="7e528-140">Om du vill stoppa programgatewayen använder du Stop-AzureApplicationGateway cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e528-140">To stop the application gateway, use the Stop-AzureApplicationGateway cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e528-141">-VnetName</span><span class="sxs-lookup"><span data-stu-id="7e528-141">-VnetName</span></span>
<span data-ttu-id="7e528-142">Anger det virtuella nätverk där denna cmdlet distribuerar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="7e528-142">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="7e528-143">Du kan inte uppdatera ett virtuellt nätverk när Application Gateway körs.</span><span class="sxs-lookup"><span data-stu-id="7e528-143">You cannot update a virtual network while the application gateway is running.</span></span>
<span data-ttu-id="7e528-144">Stoppa programgatewayen genom att använda **Stop-AzureApplicationGateway**.</span><span class="sxs-lookup"><span data-stu-id="7e528-144">To stop the application gateway, use **Stop-AzureApplicationGateway**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e528-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e528-145">CommonParameters</span></span>
<span data-ttu-id="7e528-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e528-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e528-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e528-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e528-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e528-148">INPUTS</span></span>

### <span data-ttu-id="7e528-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7e528-149">System.String</span></span>

## <span data-ttu-id="7e528-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e528-150">OUTPUTS</span></span>

### <span data-ttu-id="7e528-151">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7e528-151">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="7e528-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e528-152">NOTES</span></span>

## <span data-ttu-id="7e528-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e528-153">RELATED LINKS</span></span>

[<span data-ttu-id="7e528-154">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e528-154">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="7e528-155">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e528-155">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="7e528-156">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e528-156">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="7e528-157">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e528-157">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="7e528-158">Stopp-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e528-158">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)
