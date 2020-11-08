---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: c2c3b634eb5a9e031c375a6cc696298becd58e8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920232"
---
# <span data-ttu-id="eaaae-101">Enable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="eaaae-101">Enable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="eaaae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eaaae-102">SYNOPSIS</span></span>
<span data-ttu-id="eaaae-103">Aktiverar avancerad data säkerhet på en server.</span><span class="sxs-lookup"><span data-stu-id="eaaae-103">Enables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="eaaae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eaaae-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eaaae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eaaae-105">DESCRIPTION</span></span>
<span data-ttu-id="eaaae-106">Cmdleten **Enable-AzSqlServerAdvancedDataSecurity** aktiverar avancerad data säkerhet på en server.</span><span class="sxs-lookup"><span data-stu-id="eaaae-106">The **Enable-AzSqlServerAdvancedDataSecurity** cmdlet enables Advanced Data Security on a server.</span></span> <span data-ttu-id="eaaae-107">Avancerad data säkerhet är ett enhetligt säkerhets paket som innehåller data klassificering, sårbarhets utvärdering och Avancerat skydd för din server.</span><span class="sxs-lookup"><span data-stu-id="eaaae-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your server.</span></span> <span data-ttu-id="eaaae-108">(Ett nytt lagrings konto skapas automatiskt för att spara säkerhets utvärderingar.</span><span class="sxs-lookup"><span data-stu-id="eaaae-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="eaaae-109">Om du har skapat ett lagrings konto för detta ändamål används det i stället.</span><span class="sxs-lookup"><span data-stu-id="eaaae-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="eaaae-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eaaae-110">EXAMPLES</span></span>

### <span data-ttu-id="eaaae-111">Exempel 1-aktivera avancerad data säkerhet för servrar</span><span class="sxs-lookup"><span data-stu-id="eaaae-111">Example 1 - Enable server Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="eaaae-112">Exempel 2 – aktivera avancerad data säkerhet för servrar från Server resurs</span><span class="sxs-lookup"><span data-stu-id="eaaae-112">Example 2 - Enable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="eaaae-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eaaae-113">PARAMETERS</span></span>

### <span data-ttu-id="eaaae-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eaaae-114">-AsJob</span></span>
<span data-ttu-id="eaaae-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="eaaae-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eaaae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaaae-116">-DefaultProfile</span></span>
<span data-ttu-id="eaaae-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eaaae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaaae-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="eaaae-118">-DeploymentName</span></span>
<span data-ttu-id="eaaae-119">Ange ett namn för avancerad data säkerhets distribution</span><span class="sxs-lookup"><span data-stu-id="eaaae-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="eaaae-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="eaaae-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="eaaae-121">Tillåt inte automatiskt sårbarhets utvärdering (det här skapar inte ett lagrings konto)</span><span class="sxs-lookup"><span data-stu-id="eaaae-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="eaaae-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eaaae-122">-InputObject</span></span>
<span data-ttu-id="eaaae-123">Serverobjektet som ska användas med avancerad data säkerhets policy åtgärd</span><span class="sxs-lookup"><span data-stu-id="eaaae-123">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="eaaae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaaae-124">-ResourceGroupName</span></span>
<span data-ttu-id="eaaae-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="eaaae-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="eaaae-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eaaae-126">-ServerName</span></span>
<span data-ttu-id="eaaae-127">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="eaaae-127">SQL Database server name.</span></span>

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

### <span data-ttu-id="eaaae-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eaaae-128">-Confirm</span></span>
<span data-ttu-id="eaaae-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eaaae-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaaae-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaaae-130">-WhatIf</span></span>
<span data-ttu-id="eaaae-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eaaae-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaaae-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eaaae-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaaae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaaae-133">CommonParameters</span></span>
<span data-ttu-id="eaaae-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaaae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaaae-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaaae-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaaae-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eaaae-136">INPUTS</span></span>

### <span data-ttu-id="eaaae-137">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="eaaae-137">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="eaaae-138">System. String</span><span class="sxs-lookup"><span data-stu-id="eaaae-138">System.String</span></span>

## <span data-ttu-id="eaaae-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eaaae-139">OUTPUTS</span></span>

### <span data-ttu-id="eaaae-140">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="eaaae-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="eaaae-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eaaae-141">NOTES</span></span>

## <span data-ttu-id="eaaae-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eaaae-142">RELATED LINKS</span></span>