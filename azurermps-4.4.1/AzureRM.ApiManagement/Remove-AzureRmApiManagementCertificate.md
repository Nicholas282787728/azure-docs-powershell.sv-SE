---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 5844bbfd59e38691a28720d5cab4e73e334af88d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755514"
---
# <span data-ttu-id="c24bb-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c24bb-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="c24bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c24bb-102">SYNOPSIS</span></span>
<span data-ttu-id="c24bb-103">Tar bort ett API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="c24bb-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c24bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c24bb-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c24bb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c24bb-105">DESCRIPTION</span></span>
<span data-ttu-id="c24bb-106">Cmdleten **Remove-AzureRmApiManagementCertificate** tar bort ett Azure API Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="c24bb-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="c24bb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c24bb-107">EXAMPLES</span></span>

### <span data-ttu-id="c24bb-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="c24bb-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="c24bb-109">Det här kommandot tar bort angivet API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="c24bb-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="c24bb-110">Eftersom *Force* -parametern anges krävs ingen bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c24bb-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="c24bb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c24bb-111">PARAMETERS</span></span>

### <span data-ttu-id="c24bb-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="c24bb-112">-CertificateId</span></span>
<span data-ttu-id="c24bb-113">Anger ID för det certifikat som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c24bb-113">Specifies the ID of the certificate to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24bb-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c24bb-114">-Context</span></span>
<span data-ttu-id="c24bb-115">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c24bb-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24bb-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c24bb-116">-PassThru</span></span>
<span data-ttu-id="c24bb-117">passthru</span><span class="sxs-lookup"><span data-stu-id="c24bb-117">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24bb-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c24bb-118">-Confirm</span></span>
<span data-ttu-id="c24bb-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c24bb-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24bb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c24bb-120">-WhatIf</span></span>
<span data-ttu-id="c24bb-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c24bb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c24bb-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c24bb-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24bb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24bb-123">-DefaultProfile</span></span>
<span data-ttu-id="c24bb-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c24bb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24bb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24bb-125">CommonParameters</span></span>
<span data-ttu-id="c24bb-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c24bb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24bb-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c24bb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24bb-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c24bb-128">INPUTS</span></span>

## <span data-ttu-id="c24bb-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c24bb-129">OUTPUTS</span></span>

### <span data-ttu-id="c24bb-130">Returtyp</span><span class="sxs-lookup"><span data-stu-id="c24bb-130">Boolean</span></span>

## <span data-ttu-id="c24bb-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c24bb-131">NOTES</span></span>

## <span data-ttu-id="c24bb-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c24bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="c24bb-133">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c24bb-133">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="c24bb-134">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c24bb-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="c24bb-135">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c24bb-135">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


