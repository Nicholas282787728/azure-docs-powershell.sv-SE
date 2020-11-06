---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7cf1f52c8035adcb6dcb773106a77045525cf937
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577167"
---
# <span data-ttu-id="562fd-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="562fd-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="562fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="562fd-102">SYNOPSIS</span></span>
<span data-ttu-id="562fd-103">Lägger till ett SSL-certifikat i en programport.</span><span class="sxs-lookup"><span data-stu-id="562fd-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="562fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="562fd-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="562fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="562fd-105">DESCRIPTION</span></span>
<span data-ttu-id="562fd-106">Cmdleten **Add-AzureRmApplicationGatewaySslCertificate** lägger till ett SSL-certifikat till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="562fd-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="562fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="562fd-107">EXAMPLES</span></span>

### <span data-ttu-id="562fd-108">Exempel 1: lägga till ett SSL-certifikat till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="562fd-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="562fd-109">Det här kommandot får en Programgateway med namnet ApplicationGateway01 och lägger sedan till ett SSL-certifikat som heter Cert01.</span><span class="sxs-lookup"><span data-stu-id="562fd-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="562fd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="562fd-110">PARAMETERS</span></span>

### <span data-ttu-id="562fd-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="562fd-111">-ApplicationGateway</span></span>
<span data-ttu-id="562fd-112">Anger namnet på den Programgateway som denna cmdlet lägger till ett SSL-certifikat för.</span><span class="sxs-lookup"><span data-stu-id="562fd-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="562fd-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="562fd-113">-CertificateFile</span></span>
<span data-ttu-id="562fd-114">Anger. pfx-filen för ett SSL-certifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="562fd-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="562fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="562fd-115">-DefaultProfile</span></span>
<span data-ttu-id="562fd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="562fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="562fd-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="562fd-117">-Name</span></span>
<span data-ttu-id="562fd-118">Anger namnet på det SSL-certifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="562fd-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="562fd-119">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="562fd-119">-Password</span></span>
<span data-ttu-id="562fd-120">Anger lösen ordet för det SSL-certifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="562fd-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="562fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="562fd-121">CommonParameters</span></span>
<span data-ttu-id="562fd-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="562fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="562fd-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="562fd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="562fd-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="562fd-124">INPUTS</span></span>

### <span data-ttu-id="562fd-125">System. String</span><span class="sxs-lookup"><span data-stu-id="562fd-125">System.String</span></span>

## <span data-ttu-id="562fd-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="562fd-126">OUTPUTS</span></span>

### <span data-ttu-id="562fd-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="562fd-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="562fd-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="562fd-128">NOTES</span></span>

## <span data-ttu-id="562fd-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="562fd-129">RELATED LINKS</span></span>

[<span data-ttu-id="562fd-130">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="562fd-130">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="562fd-131">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="562fd-131">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="562fd-132">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="562fd-132">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="562fd-133">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="562fd-133">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


