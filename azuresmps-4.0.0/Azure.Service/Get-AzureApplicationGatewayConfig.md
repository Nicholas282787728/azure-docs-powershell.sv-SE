---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093391"
---
# <span data-ttu-id="bd42a-101">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="bd42a-101">Get-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="bd42a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd42a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd42a-103">Hämtar en konfigurations kontext för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="bd42a-103">Gets an Application Gateway configuration context.</span></span>

## <span data-ttu-id="bd42a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd42a-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd42a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd42a-105">DESCRIPTION</span></span>
<span data-ttu-id="bd42a-106">Cmdleten **Get-AzureApplicationGatewayConfig** hämtar en konfigurations kontext för Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bd42a-106">The **Get-AzureApplicationGatewayConfig** cmdlet gets an Azure Application Gateway configuration context.</span></span>
<span data-ttu-id="bd42a-107">En kontext innehåller både ett konfigurations objekt och en XML-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bd42a-107">A context includes both a configuration object and XML configuration.</span></span>
<span data-ttu-id="bd42a-108">Du kan spara XML-konfigurationen i en fil.</span><span class="sxs-lookup"><span data-stu-id="bd42a-108">You can save the XML configuration to a file.</span></span>

## <span data-ttu-id="bd42a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd42a-109">EXAMPLES</span></span>

### <span data-ttu-id="bd42a-110">Exempel 1: Hämta en konfiguration för Programgateway och spara den i en fil</span><span class="sxs-lookup"><span data-stu-id="bd42a-110">Example 1: Get an Application Gateway configuration and save it to a file</span></span>
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

<span data-ttu-id="bd42a-111">Det här kommandot hämtar konfigurationen för en Programgateway som heter ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="bd42a-111">This command gets the configuration for an Application Gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="bd42a-112">Kommandot sparar det i filen på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="bd42a-112">The command saves it in the file in the specified path.</span></span>

## <span data-ttu-id="bd42a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd42a-113">PARAMETERS</span></span>

### <span data-ttu-id="bd42a-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="bd42a-114">-ExportToFile</span></span>
<span data-ttu-id="bd42a-115">Anger en fil Sök väg som den här cmdleten sparar konfigurationen i XML-format för.</span><span class="sxs-lookup"><span data-stu-id="bd42a-115">Specifies a file path to which this cmdlet saves the configuration in XML format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd42a-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd42a-116">-Name</span></span>
<span data-ttu-id="bd42a-117">Anger namnet på den Programgateway för vilken denna cmdlet hämtar konfigurations information.</span><span class="sxs-lookup"><span data-stu-id="bd42a-117">Specifies the name of the Application Gateway for which this cmdlet gets configuration information.</span></span>

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

### <span data-ttu-id="bd42a-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="bd42a-118">-Profile</span></span>
<span data-ttu-id="bd42a-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="bd42a-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bd42a-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="bd42a-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bd42a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd42a-121">CommonParameters</span></span>
<span data-ttu-id="bd42a-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd42a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd42a-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd42a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd42a-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd42a-124">INPUTS</span></span>

### <span data-ttu-id="bd42a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bd42a-125">System.String</span></span>

## <span data-ttu-id="bd42a-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd42a-126">OUTPUTS</span></span>

### <span data-ttu-id="bd42a-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext</span><span class="sxs-lookup"><span data-stu-id="bd42a-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfigContext</span></span>

## <span data-ttu-id="bd42a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd42a-128">NOTES</span></span>

## <span data-ttu-id="bd42a-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd42a-129">RELATED LINKS</span></span>

[<span data-ttu-id="bd42a-130">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="bd42a-130">Set-AzureApplicationGatewayConfig</span></span>](./Set-AzureApplicationGatewayConfig.md)


