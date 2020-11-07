---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: 65c178cc8cf293cf6c20e6262733031e377f61fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929050"
---
# <span data-ttu-id="4d856-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4d856-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="4d856-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d856-102">SYNOPSIS</span></span>
<span data-ttu-id="4d856-103">Lägger till ett SSL-certifikat i en programport.</span><span class="sxs-lookup"><span data-stu-id="4d856-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d856-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d856-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d856-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d856-105">DESCRIPTION</span></span>
<span data-ttu-id="4d856-106">Cmdleten **Add-AzureRmApplicationGatewaySslCertificate** lägger till ett SSL-certifikat till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4d856-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="4d856-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d856-107">EXAMPLES</span></span>

### <span data-ttu-id="4d856-108">Exempel 1: lägga till ett SSL-certifikat till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4d856-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="4d856-109">Det här kommandot får en Programgateway med namnet ApplicationGateway01 och lägger sedan till ett SSL-certifikat som heter Cert01.</span><span class="sxs-lookup"><span data-stu-id="4d856-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="4d856-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d856-110">PARAMETERS</span></span>

### <span data-ttu-id="4d856-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d856-111">-ApplicationGateway</span></span>
<span data-ttu-id="4d856-112">Anger namnet på den Programgateway som denna cmdlet lägger till ett SSL-certifikat för.</span><span class="sxs-lookup"><span data-stu-id="4d856-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="4d856-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4d856-113">-CertificateFile</span></span>
<span data-ttu-id="4d856-114">Anger. pfx-filen för ett SSL-certifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="4d856-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4d856-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d856-115">-DefaultProfile</span></span>
<span data-ttu-id="4d856-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d856-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d856-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d856-117">-Name</span></span>
<span data-ttu-id="4d856-118">Anger namnet på det SSL-certifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="4d856-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4d856-119">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="4d856-119">-Password</span></span>
<span data-ttu-id="4d856-120">Anger lösen ordet för det SSL-certifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="4d856-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4d856-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d856-121">CommonParameters</span></span>
<span data-ttu-id="4d856-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d856-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d856-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d856-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d856-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d856-124">INPUTS</span></span>

### <span data-ttu-id="4d856-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4d856-125">System.String</span></span>

## <span data-ttu-id="4d856-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d856-126">OUTPUTS</span></span>

### <span data-ttu-id="4d856-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d856-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d856-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d856-128">NOTES</span></span>

## <span data-ttu-id="4d856-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d856-129">RELATED LINKS</span></span>

[<span data-ttu-id="4d856-130">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4d856-130">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4d856-131">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4d856-131">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4d856-132">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4d856-132">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4d856-133">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4d856-133">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


