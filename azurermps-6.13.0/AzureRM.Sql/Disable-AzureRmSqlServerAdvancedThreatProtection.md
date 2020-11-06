---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/disable-azurermsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Disable-AzureRmSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Disable-AzureRmSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: cc38d619b810f2567594c0c1020190c271dc9f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576054"
---
# <span data-ttu-id="5e39d-101">Disable-AzureRmSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5e39d-101">Disable-AzureRmSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="5e39d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e39d-102">SYNOPSIS</span></span>
<span data-ttu-id="5e39d-103">Inaktiverar Avancerat skydd på en server.</span><span class="sxs-lookup"><span data-stu-id="5e39d-103">Disables Advanced Threat Protection on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e39d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e39d-104">SYNTAX</span></span>

```
Disable-AzureRmSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e39d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e39d-105">DESCRIPTION</span></span>
<span data-ttu-id="5e39d-106">Cmdleten **disable-AzureRmSqlServerAdvancedThreatProtection** inaktiverar Avancerat skydd mot en server.</span><span class="sxs-lookup"><span data-stu-id="5e39d-106">The **Disable-AzureRmSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="5e39d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e39d-107">EXAMPLES</span></span>

### <span data-ttu-id="5e39d-108">Exempel 1 – inaktivera Avancerat skydd för Server</span><span class="sxs-lookup"><span data-stu-id="5e39d-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzureRmSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="5e39d-109">Exempel 2 – inaktivera Avancerat skydd för Server från Server resurs</span><span class="sxs-lookup"><span data-stu-id="5e39d-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzureRmSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="5e39d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e39d-110">PARAMETERS</span></span>

### <span data-ttu-id="5e39d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e39d-111">-DefaultProfile</span></span>
<span data-ttu-id="5e39d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e39d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e39d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e39d-113">-InputObject</span></span>
<span data-ttu-id="5e39d-114">Serverobjektet som ska användas med åtgärden för avancerad skydds policy</span><span class="sxs-lookup"><span data-stu-id="5e39d-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="5e39d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e39d-115">-ResourceGroupName</span></span>
<span data-ttu-id="5e39d-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5e39d-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e39d-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e39d-117">-ServerName</span></span>
<span data-ttu-id="5e39d-118">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="5e39d-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="5e39d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e39d-119">-Confirm</span></span>
<span data-ttu-id="5e39d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e39d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e39d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e39d-121">-WhatIf</span></span>
<span data-ttu-id="5e39d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e39d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e39d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e39d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e39d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e39d-124">CommonParameters</span></span>
<span data-ttu-id="5e39d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e39d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e39d-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e39d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e39d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e39d-127">INPUTS</span></span>

### <span data-ttu-id="5e39d-128">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5e39d-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="5e39d-129">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5e39d-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5e39d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5e39d-130">System.String</span></span>

## <span data-ttu-id="5e39d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e39d-131">OUTPUTS</span></span>

### <span data-ttu-id="5e39d-132">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5e39d-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="5e39d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e39d-133">NOTES</span></span>

## <span data-ttu-id="5e39d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e39d-134">RELATED LINKS</span></span>
