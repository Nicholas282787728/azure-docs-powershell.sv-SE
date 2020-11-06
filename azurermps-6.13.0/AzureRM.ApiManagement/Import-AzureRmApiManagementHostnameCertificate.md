---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementhostnamecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 80bc75e8029db9aa4cac9f1e0abd53ad17c9fad1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576352"
---
# <span data-ttu-id="0f65d-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="0f65d-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="0f65d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f65d-102">SYNOPSIS</span></span>
<span data-ttu-id="0f65d-103">Importerar ett certifikat i ett PFX-format för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0f65d-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f65d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f65d-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f65d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f65d-105">DESCRIPTION</span></span>
<span data-ttu-id="0f65d-106">Cmdleten **import-AzureRmApiManagementHostnameCertificate** importerar ett certifikat i PFX-format för API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="0f65d-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="0f65d-107">Certifikatet ska användas för konfiguration av anpassade värdnamn.</span><span class="sxs-lookup"><span data-stu-id="0f65d-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="0f65d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f65d-108">EXAMPLES</span></span>

### <span data-ttu-id="0f65d-109">Exempel 1: importera ett värd certifikat för API-hantering</span><span class="sxs-lookup"><span data-stu-id="0f65d-109">Example 1: Import a API Management hostname certificate</span></span>
```powershell
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="0f65d-110">Det här kommandot importerar ett certifikat för ett anpassat proxykonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0f65d-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="0f65d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f65d-111">PARAMETERS</span></span>

### <span data-ttu-id="0f65d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f65d-112">-DefaultProfile</span></span>
<span data-ttu-id="0f65d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f65d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f65d-114">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="0f65d-114">-HostnameType</span></span>
<span data-ttu-id="0f65d-115">Anger den typ av värdnamn som denna cmdlet läser in certifikatet för.</span><span class="sxs-lookup"><span data-stu-id="0f65d-115">Specifies the host name type that this cmdlet loads the certificate for.</span></span>
<span data-ttu-id="0f65d-116">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="0f65d-116">Valid values are:</span></span> 
- <span data-ttu-id="0f65d-117">Identifiera</span><span class="sxs-lookup"><span data-stu-id="0f65d-117">Proxy</span></span>
- <span data-ttu-id="0f65d-118">Portalen</span><span class="sxs-lookup"><span data-stu-id="0f65d-118">Portal</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f65d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f65d-119">-Name</span></span>
<span data-ttu-id="0f65d-120">Anger namnet på den API-hanterings distribution som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="0f65d-120">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

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

### <span data-ttu-id="0f65d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f65d-121">-PassThru</span></span>
<span data-ttu-id="0f65d-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0f65d-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f65d-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0f65d-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f65d-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="0f65d-124">-PfxPassword</span></span>
<span data-ttu-id="0f65d-125">Anger lösen ordet för. pfx-filen.</span><span class="sxs-lookup"><span data-stu-id="0f65d-125">Specifies the password for the .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f65d-126">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="0f65d-126">-PfxPath</span></span>
<span data-ttu-id="0f65d-127">Anger sökvägen till en. pfx-fil.</span><span class="sxs-lookup"><span data-stu-id="0f65d-127">Specifies the path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f65d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f65d-128">-ResourceGroupName</span></span>
<span data-ttu-id="0f65d-129">Anger namnet på den resurs grupp som distributionen av API-hanteringen finns under.</span><span class="sxs-lookup"><span data-stu-id="0f65d-129">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="0f65d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f65d-130">CommonParameters</span></span>
<span data-ttu-id="0f65d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f65d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f65d-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f65d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f65d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f65d-133">INPUTS</span></span>

### <span data-ttu-id="0f65d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0f65d-134">System.String</span></span>

### <span data-ttu-id="0f65d-135">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementHostnameType</span><span class="sxs-lookup"><span data-stu-id="0f65d-135">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType</span></span>

## <span data-ttu-id="0f65d-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f65d-136">OUTPUTS</span></span>

### <span data-ttu-id="0f65d-137">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="0f65d-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="0f65d-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f65d-138">NOTES</span></span>

## <span data-ttu-id="0f65d-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f65d-139">RELATED LINKS</span></span>

[<span data-ttu-id="0f65d-140">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f65d-140">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="0f65d-141">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="0f65d-141">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


