---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: 3e3fea3e43f2370347ae819604d6caf1e830ebd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579863"
---
# <span data-ttu-id="4fb27-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="4fb27-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="4fb27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fb27-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb27-103">Anger en anpassad värdnamn-konfiguration för en proxy eller portal för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4fb27-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fb27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fb27-104">SYNTAX</span></span>

### <span data-ttu-id="4fb27-105">Specifik API-hanterings tjänst (standard)</span><span class="sxs-lookup"><span data-stu-id="4fb27-105">Specific API Management service (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fb27-106">Ange från angiven PsApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="4fb27-106">Set from provided PsApiManagement instance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fb27-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fb27-107">DESCRIPTION</span></span>
<span data-ttu-id="4fb27-108">Cmdleten **set-AzureRmApiManagementHostnames** tillämpar en anpassad värdnamn konfiguration för en proxy eller portal för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4fb27-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="4fb27-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fb27-109">EXAMPLES</span></span>

### <span data-ttu-id="4fb27-110">Exempel 1: Ange den anpassade värd konfigurations konfigurationen för en proxy och Portal</span><span class="sxs-lookup"><span data-stu-id="4fb27-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="4fb27-111">Det här kommandot ställer in den anpassade värd konfigurations konfigurationen för proxy och Portal.</span><span class="sxs-lookup"><span data-stu-id="4fb27-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="4fb27-112">Exempel 2: Konfigurera ett anpassat värdnamn för en proxy och Portal</span><span class="sxs-lookup"><span data-stu-id="4fb27-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="4fb27-113">Det här exemplet konfigurerar ett anpassat värd namn för proxy och Portal.</span><span class="sxs-lookup"><span data-stu-id="4fb27-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="4fb27-114">Du måste importera motsvarande certifikat och sedan använda de anpassade värderna.</span><span class="sxs-lookup"><span data-stu-id="4fb27-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="4fb27-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fb27-115">PARAMETERS</span></span>

### <span data-ttu-id="4fb27-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fb27-116">-ApiManagement</span></span>
<span data-ttu-id="4fb27-117">Anger den **PsApiManagement** -instans som den här cmdleten hämtar *PortalHostnameConfiguration* -och *ProxyHostnameConfiguration* -parametrarna från.</span><span class="sxs-lookup"><span data-stu-id="4fb27-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Set from provided PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb27-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4fb27-118">-Name</span></span>
<span data-ttu-id="4fb27-119">Anger namnet på API-hanterings instansen.</span><span class="sxs-lookup"><span data-stu-id="4fb27-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb27-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fb27-120">-PassThru</span></span>
<span data-ttu-id="4fb27-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="4fb27-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4fb27-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4fb27-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4fb27-123">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fb27-123">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="4fb27-124">Anger konfiguration för anpassad Portal-värdnamn.</span><span class="sxs-lookup"><span data-stu-id="4fb27-124">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="4fb27-125">Om du skickar $null till cmdleten anges standard värd namnet.</span><span class="sxs-lookup"><span data-stu-id="4fb27-125">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb27-126">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fb27-126">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="4fb27-127">Anger konfiguration för anpassad proxykonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4fb27-127">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="4fb27-128">Om du skickar $null ange standard namnet.</span><span class="sxs-lookup"><span data-stu-id="4fb27-128">Passing $null sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb27-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb27-129">-ResourceGroupName</span></span>
<span data-ttu-id="4fb27-130">Anger namnet på resurs gruppen som API-hanterings instans finns under.</span><span class="sxs-lookup"><span data-stu-id="4fb27-130">Specifies the name of the resource group under which the API Management instance exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb27-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb27-131">-DefaultProfile</span></span>
<span data-ttu-id="4fb27-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb27-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fb27-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb27-133">CommonParameters</span></span>
<span data-ttu-id="4fb27-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb27-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb27-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb27-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb27-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fb27-136">INPUTS</span></span>

### <span data-ttu-id="4fb27-137">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fb27-137">PsApiManagement</span></span>
<span data-ttu-id="4fb27-138">Parametern ' ApiManagement ' godkänner värdet av typen ' PsApiManagement ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4fb27-138">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="4fb27-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fb27-139">OUTPUTS</span></span>

### <span data-ttu-id="4fb27-140">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fb27-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="4fb27-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fb27-141">NOTES</span></span>

## <span data-ttu-id="4fb27-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fb27-142">RELATED LINKS</span></span>

[<span data-ttu-id="4fb27-143">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="4fb27-143">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="4fb27-144">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fb27-144">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)


