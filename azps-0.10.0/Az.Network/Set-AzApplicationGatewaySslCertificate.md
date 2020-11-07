---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b68f0bf3b0112587256fddc3dbb6c31605f811b7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924245"
---
# <span data-ttu-id="c3f72-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c3f72-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c3f72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3f72-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f72-103">Anger mål tillstånd för ett SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="c3f72-103">Sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="c3f72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3f72-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3f72-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3f72-105">DESCRIPTION</span></span>
<span data-ttu-id="c3f72-106">Cmdleten **set-AzApplicationGatewaySslCertificate** anger mål tillståndet för ett SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="c3f72-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="c3f72-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3f72-107">EXAMPLES</span></span>

### <span data-ttu-id="c3f72-108">Exempel 1: Ange mål tillstånd för ett SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="c3f72-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="c3f72-109">Det här kommandot anger mål tillståndet för ett SSL-certifikat från den Programgateway som heter ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="c3f72-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="c3f72-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3f72-110">PARAMETERS</span></span>

### <span data-ttu-id="c3f72-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3f72-111">-ApplicationGateway</span></span>
<span data-ttu-id="c3f72-112">Anger den Programgateway som certifikatet för SSL (Secure Socket Layer) är associerat med.</span><span class="sxs-lookup"><span data-stu-id="c3f72-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="c3f72-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c3f72-113">-CertificateFile</span></span>
<span data-ttu-id="c3f72-114">Anger sökvägen till SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c3f72-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="c3f72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f72-115">-DefaultProfile</span></span>
<span data-ttu-id="c3f72-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3f72-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3f72-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3f72-117">-Name</span></span>
<span data-ttu-id="c3f72-118">Anger namnet på SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c3f72-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="c3f72-119">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="c3f72-119">-Password</span></span>
<span data-ttu-id="c3f72-120">Anger lösen ordet för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c3f72-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="c3f72-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f72-121">CommonParameters</span></span>
<span data-ttu-id="c3f72-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3f72-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f72-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3f72-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f72-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3f72-124">INPUTS</span></span>

### <span data-ttu-id="c3f72-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c3f72-125">System.String</span></span>

## <span data-ttu-id="c3f72-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3f72-126">OUTPUTS</span></span>

### <span data-ttu-id="c3f72-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3f72-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3f72-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3f72-128">NOTES</span></span>

## <span data-ttu-id="c3f72-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3f72-129">RELATED LINKS</span></span>

[<span data-ttu-id="c3f72-130">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c3f72-130">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c3f72-131">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c3f72-131">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c3f72-132">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c3f72-132">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c3f72-133">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c3f72-133">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


