---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099659"
---
# <span data-ttu-id="f3cd0-101">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="f3cd0-101">Set-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="f3cd0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="f3cd0-103">Konfigurerar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-103">Configures an application gateway.</span></span>

## <span data-ttu-id="f3cd0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3cd0-104">SYNTAX</span></span>

### <span data-ttu-id="f3cd0-105">configFile</span><span class="sxs-lookup"><span data-stu-id="f3cd0-105">configFile</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cd0-106">configObject</span><span class="sxs-lookup"><span data-stu-id="f3cd0-106">configObject</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f3cd0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3cd0-107">DESCRIPTION</span></span>
<span data-ttu-id="f3cd0-108">Cmdleten **set-AzureApplicationGatewayConfig** konfigurerar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-108">The **Set-AzureApplicationGatewayConfig** cmdlet configures an application gateway.</span></span>

## <span data-ttu-id="f3cd0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3cd0-109">EXAMPLES</span></span>

### <span data-ttu-id="f3cd0-110">Exempel 1: Konfigurera en Programgateway genom att använda ett konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="f3cd0-110">Example 1: Configure an application gateway by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

<span data-ttu-id="f3cd0-111">Det första kommandot får konfigurationsobjektet för den Programgateway som heter ApplicationGateway02 med hjälp av cmdleten **Get-AzureApplicationGatewayConfig** .</span><span class="sxs-lookup"><span data-stu-id="f3cd0-111">The first command gets the configuration object for the application gateway named ApplicationGateway02 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="f3cd0-112">Kommandot sparar det i $ConfigReturnObject variabel.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-112">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="f3cd0-113">Det andra kommandot anger konfigurationen för programmet som heter ApplicationGateway06 genom att använda ett konfigurations objekt för Programgateway som lagras i $ConfigReturnObject variabeln.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-113">The second command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration object stored in the $ConfigReturnObject variable.</span></span>

### <span data-ttu-id="f3cd0-114">Exempel 2: Konfigurera en Programgateway genom att använda en konfigurations fil</span><span class="sxs-lookup"><span data-stu-id="f3cd0-114">Example 2: Configure an application gateway by using a configuration file</span></span>
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

<span data-ttu-id="f3cd0-115">Det här kommandot anger konfigurationen för programmet med namnet ApplicationGateway06 genom att använda en konfigurations fil för Programgateway på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-115">This command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration file in the specified location.</span></span>

### <span data-ttu-id="f3cd0-116">Exempel 3: ändra en konfiguration genom att använda ett konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="f3cd0-116">Example 3: Modify a configuration by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

<span data-ttu-id="f3cd0-117">Det första kommandot får konfigurationsobjektet för den Programgateway som heter ApplicationGateway06 med hjälp av cmdleten **Get-AzureApplicationGatewayConfig** .</span><span class="sxs-lookup"><span data-stu-id="f3cd0-117">The first command gets the configuration object for the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="f3cd0-118">Kommandot sparar det i $ConfigReturnObject variabel.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-118">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="f3cd0-119">Det andra kommandot tilldelar ett port värde till en **port** egenskap i objektet som lagras i $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-119">The second command assigns a port value to a **Port** property in the object stored in $ConfigReturnObject.</span></span>

<span data-ttu-id="f3cd0-120">Det sista kommandot skickar den uppdaterade $ConfigReturnObject till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-120">The final command passes the updated $ConfigReturnObject to the current cmdlet.</span></span>

## <span data-ttu-id="f3cd0-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3cd0-121">PARAMETERS</span></span>

### <span data-ttu-id="f3cd0-122">-Config</span><span class="sxs-lookup"><span data-stu-id="f3cd0-122">-Config</span></span>
<span data-ttu-id="f3cd0-123">Anger ett konfigurations objekt för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-123">Specifies an application gateway configuration object.</span></span>
<span data-ttu-id="f3cd0-124">Denna cmdlet tilldelar den konfiguration som den här parametern anger till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-124">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cd0-125">-ConfigFile</span><span class="sxs-lookup"><span data-stu-id="f3cd0-125">-ConfigFile</span></span>
<span data-ttu-id="f3cd0-126">Anger sökvägen till en konfigurations fil i XML-format för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-126">Specifies the path of a configuration file, in XML format, for an application gateway.</span></span>
<span data-ttu-id="f3cd0-127">Denna cmdlet tilldelar den konfiguration som den här parametern anger till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-127">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cd0-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3cd0-128">-Name</span></span>
<span data-ttu-id="f3cd0-129">Anger namnet på den Application Gateway som denna cmdlet konfigurerar.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-129">Specifies the name of the application gateway that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3cd0-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="f3cd0-130">-Profile</span></span>
<span data-ttu-id="f3cd0-131">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-131">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f3cd0-132">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3cd0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3cd0-133">CommonParameters</span></span>
<span data-ttu-id="f3cd0-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3cd0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3cd0-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3cd0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3cd0-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3cd0-136">INPUTS</span></span>

### <span data-ttu-id="f3cd0-137">System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3cd0-137">System.String, Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfiguration</span></span>

## <span data-ttu-id="f3cd0-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3cd0-138">OUTPUTS</span></span>

### <span data-ttu-id="f3cd0-139">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f3cd0-139">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="f3cd0-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3cd0-140">NOTES</span></span>

## <span data-ttu-id="f3cd0-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3cd0-141">RELATED LINKS</span></span>

[<span data-ttu-id="f3cd0-142">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="f3cd0-142">Get-AzureApplicationGatewayConfig</span></span>](./Get-AzureApplicationGatewayConfig.md)


