---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: a333f3e5263f565a44856a9af43be272cc971a22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755780"
---
# <span data-ttu-id="8fad6-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8fad6-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="8fad6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fad6-102">SYNOPSIS</span></span>
<span data-ttu-id="8fad6-103">Tar bort ett API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="8fad6-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fad6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fad6-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fad6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fad6-105">DESCRIPTION</span></span>
<span data-ttu-id="8fad6-106">Cmdleten **Remove-AzureRmApiManagementCertificate** tar bort ett Azure API Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="8fad6-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="8fad6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fad6-107">EXAMPLES</span></span>

### <span data-ttu-id="8fad6-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="8fad6-108">Example 1: Remove a certificate</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="8fad6-109">Det här kommandot tar bort angivet API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="8fad6-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="8fad6-110">Eftersom *Force* -parametern anges krävs ingen bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8fad6-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="8fad6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fad6-111">PARAMETERS</span></span>

### <span data-ttu-id="8fad6-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="8fad6-112">-CertificateId</span></span>
<span data-ttu-id="8fad6-113">Anger ID för det certifikat som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8fad6-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="8fad6-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8fad6-114">-Context</span></span>
<span data-ttu-id="8fad6-115">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8fad6-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8fad6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fad6-116">-DefaultProfile</span></span>
<span data-ttu-id="8fad6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fad6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="8fad6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fad6-118">-PassThru</span></span>
<span data-ttu-id="8fad6-119">passthru</span><span class="sxs-lookup"><span data-stu-id="8fad6-119">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fad6-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8fad6-120">-Confirm</span></span>
<span data-ttu-id="8fad6-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8fad6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fad6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fad6-122">-WhatIf</span></span>
<span data-ttu-id="8fad6-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8fad6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fad6-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8fad6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fad6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fad6-125">CommonParameters</span></span>
<span data-ttu-id="8fad6-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fad6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fad6-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fad6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fad6-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fad6-128">INPUTS</span></span>

### <span data-ttu-id="8fad6-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="8fad6-129">None</span></span>
<span data-ttu-id="8fad6-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8fad6-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8fad6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fad6-131">OUTPUTS</span></span>

### <span data-ttu-id="8fad6-132">Returtyp</span><span class="sxs-lookup"><span data-stu-id="8fad6-132">Boolean</span></span>

## <span data-ttu-id="8fad6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fad6-133">NOTES</span></span>

## <span data-ttu-id="8fad6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fad6-134">RELATED LINKS</span></span>

[<span data-ttu-id="8fad6-135">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8fad6-135">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="8fad6-136">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8fad6-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="8fad6-137">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8fad6-137">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


