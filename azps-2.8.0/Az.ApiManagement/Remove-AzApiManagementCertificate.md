---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: fc22515fc1d1fc4c3975ee315ec9f7bf611e67c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745712"
---
# <span data-ttu-id="2cbd7-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2cbd7-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="2cbd7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2cbd7-102">SYNOPSIS</span></span>
<span data-ttu-id="2cbd7-103">Tar bort ett API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="2cbd7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2cbd7-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cbd7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2cbd7-105">DESCRIPTION</span></span>
<span data-ttu-id="2cbd7-106">Cmdleten **Remove-AzApiManagementCertificate** tar bort ett Azure API Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="2cbd7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2cbd7-107">EXAMPLES</span></span>

### <span data-ttu-id="2cbd7-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="2cbd7-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="2cbd7-109">Det här kommandot tar bort angivet API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="2cbd7-110">Eftersom *Force* -parametern anges krävs ingen bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="2cbd7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2cbd7-111">PARAMETERS</span></span>

### <span data-ttu-id="2cbd7-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="2cbd7-112">-CertificateId</span></span>
<span data-ttu-id="2cbd7-113">Anger ID för det certifikat som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="2cbd7-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2cbd7-114">-Context</span></span>
<span data-ttu-id="2cbd7-115">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbd7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cbd7-116">-DefaultProfile</span></span>
<span data-ttu-id="2cbd7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cbd7-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cbd7-118">-PassThru</span></span>
<span data-ttu-id="2cbd7-119">passthru</span><span class="sxs-lookup"><span data-stu-id="2cbd7-119">passthru</span></span>

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

### <span data-ttu-id="2cbd7-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2cbd7-120">-Confirm</span></span>
<span data-ttu-id="2cbd7-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cbd7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cbd7-122">-WhatIf</span></span>
<span data-ttu-id="2cbd7-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cbd7-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cbd7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cbd7-125">CommonParameters</span></span>
<span data-ttu-id="2cbd7-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cbd7-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cbd7-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cbd7-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2cbd7-128">INPUTS</span></span>

### <span data-ttu-id="2cbd7-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2cbd7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2cbd7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2cbd7-130">System.String</span></span>

### <span data-ttu-id="2cbd7-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2cbd7-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2cbd7-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2cbd7-132">OUTPUTS</span></span>

### <span data-ttu-id="2cbd7-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2cbd7-133">System.Boolean</span></span>

## <span data-ttu-id="2cbd7-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2cbd7-134">NOTES</span></span>

## <span data-ttu-id="2cbd7-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2cbd7-135">RELATED LINKS</span></span>

[<span data-ttu-id="2cbd7-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2cbd7-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="2cbd7-137">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2cbd7-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="2cbd7-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2cbd7-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


