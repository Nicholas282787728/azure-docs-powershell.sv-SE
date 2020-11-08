---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 36efc8b3dfec4bcc126191d68c04c2cd5d071fbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089306"
---
# <span data-ttu-id="f031f-101">Enable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="f031f-101">Enable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="f031f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f031f-102">SYNOPSIS</span></span>
<span data-ttu-id="f031f-103">Aktiverar avancerad data säkerhet på en server.</span><span class="sxs-lookup"><span data-stu-id="f031f-103">Enables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="f031f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f031f-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f031f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f031f-105">DESCRIPTION</span></span>
<span data-ttu-id="f031f-106">Cmdleten **Enable-AzSqlServerAdvancedDataSecurity** aktiverar avancerad data säkerhet på en server.</span><span class="sxs-lookup"><span data-stu-id="f031f-106">The **Enable-AzSqlServerAdvancedDataSecurity** cmdlet enables Advanced Data Security on a server.</span></span> <span data-ttu-id="f031f-107">Avancerad data säkerhet är ett enhetligt säkerhets paket som innehåller data klassificering, sårbarhets utvärdering och Avancerat skydd för din server.</span><span class="sxs-lookup"><span data-stu-id="f031f-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your server.</span></span> <span data-ttu-id="f031f-108">(Ett nytt lagrings konto skapas automatiskt för att spara säkerhets utvärderingar.</span><span class="sxs-lookup"><span data-stu-id="f031f-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="f031f-109">Om du har skapat ett lagrings konto för detta ändamål används det i stället.</span><span class="sxs-lookup"><span data-stu-id="f031f-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="f031f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f031f-110">EXAMPLES</span></span>

### <span data-ttu-id="f031f-111">Exempel 1-aktivera avancerad data säkerhet för servrar</span><span class="sxs-lookup"><span data-stu-id="f031f-111">Example 1 - Enable server Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="f031f-112">Exempel 2 – aktivera avancerad data säkerhet för servrar från Server resurs</span><span class="sxs-lookup"><span data-stu-id="f031f-112">Example 2 - Enable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="f031f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f031f-113">PARAMETERS</span></span>

### <span data-ttu-id="f031f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f031f-114">-AsJob</span></span>
<span data-ttu-id="f031f-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f031f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f031f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f031f-116">-DefaultProfile</span></span>
<span data-ttu-id="f031f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f031f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f031f-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="f031f-118">-DeploymentName</span></span>
<span data-ttu-id="f031f-119">Ange ett namn för avancerad data säkerhets distribution</span><span class="sxs-lookup"><span data-stu-id="f031f-119">Supply a custom name for Advanced Data Security deployment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f031f-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="f031f-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="f031f-121">Tillåt inte automatiskt sårbarhets utvärdering (det här skapar inte ett lagrings konto)</span><span class="sxs-lookup"><span data-stu-id="f031f-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="f031f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f031f-122">-InputObject</span></span>
<span data-ttu-id="f031f-123">Serverobjektet som ska användas med avancerad data säkerhets policy åtgärd</span><span class="sxs-lookup"><span data-stu-id="f031f-123">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f031f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f031f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f031f-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f031f-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f031f-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f031f-126">-ServerName</span></span>
<span data-ttu-id="f031f-127">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f031f-127">SQL Database server name.</span></span>

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

### <span data-ttu-id="f031f-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f031f-128">-Confirm</span></span>
<span data-ttu-id="f031f-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f031f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f031f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f031f-130">-WhatIf</span></span>
<span data-ttu-id="f031f-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f031f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f031f-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f031f-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f031f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f031f-133">CommonParameters</span></span>
<span data-ttu-id="f031f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f031f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f031f-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f031f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f031f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f031f-136">INPUTS</span></span>

### <span data-ttu-id="f031f-137">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f031f-137">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="f031f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f031f-138">System.String</span></span>

## <span data-ttu-id="f031f-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f031f-139">OUTPUTS</span></span>

### <span data-ttu-id="f031f-140">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f031f-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="f031f-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f031f-141">NOTES</span></span>

## <span data-ttu-id="f031f-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f031f-142">RELATED LINKS</span></span>
