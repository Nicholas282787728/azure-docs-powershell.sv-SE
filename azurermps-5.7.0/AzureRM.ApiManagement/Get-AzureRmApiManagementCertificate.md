---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: b6825d23244664b475dbd28472dc30f33117a59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756517"
---
# <span data-ttu-id="2f235-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2f235-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="2f235-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f235-102">SYNOPSIS</span></span>
<span data-ttu-id="2f235-103">Får API-Management-certifikat konfigurerade för ömsesidig autentisering med Server delen i tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2f235-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f235-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f235-104">SYNTAX</span></span>

### <span data-ttu-id="2f235-105">GetAllCertificates (standard)</span><span class="sxs-lookup"><span data-stu-id="2f235-105">GetAllCertificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f235-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="2f235-106">GetByCertificateId</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f235-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f235-107">DESCRIPTION</span></span>
<span data-ttu-id="2f235-108">Cmdleten **Get-AzureRmApiManagementCertificate** får alla Azure API Management-certifikat eller certifikat som du anger.</span><span class="sxs-lookup"><span data-stu-id="2f235-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="2f235-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f235-109">EXAMPLES</span></span>

### <span data-ttu-id="2f235-110">Exempel 1: Hämta alla certifikat</span><span class="sxs-lookup"><span data-stu-id="2f235-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="2f235-111">Det här kommandot får alla API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="2f235-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="2f235-112">Exempel 2: skaffa ett certifikat utifrån dess ID</span><span class="sxs-lookup"><span data-stu-id="2f235-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="2f235-113">Det här kommandot får API-hanteringskonsolen med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="2f235-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="2f235-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f235-114">PARAMETERS</span></span>

### <span data-ttu-id="2f235-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="2f235-115">-CertificateId</span></span>
<span data-ttu-id="2f235-116">Anger ID för det certifikat som ska visas.</span><span class="sxs-lookup"><span data-stu-id="2f235-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByCertificateId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f235-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2f235-117">-Context</span></span>
<span data-ttu-id="2f235-118">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2f235-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f235-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f235-119">-DefaultProfile</span></span>
<span data-ttu-id="2f235-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f235-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2f235-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f235-121">-Confirm</span></span>
<span data-ttu-id="2f235-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f235-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f235-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f235-123">-WhatIf</span></span>
<span data-ttu-id="2f235-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f235-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f235-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f235-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f235-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f235-126">CommonParameters</span></span>
<span data-ttu-id="2f235-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f235-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f235-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f235-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f235-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f235-129">INPUTS</span></span>

### <span data-ttu-id="2f235-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="2f235-130">None</span></span>
<span data-ttu-id="2f235-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2f235-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f235-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f235-132">OUTPUTS</span></span>

### <span data-ttu-id="2f235-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2f235-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="2f235-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f235-134">NOTES</span></span>

## <span data-ttu-id="2f235-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f235-135">RELATED LINKS</span></span>

[<span data-ttu-id="2f235-136">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2f235-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="2f235-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2f235-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="2f235-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2f235-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


