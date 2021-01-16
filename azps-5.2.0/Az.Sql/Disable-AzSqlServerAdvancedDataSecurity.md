---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 5dd2c495fa80826f88f96901df7a02ad33bf8e4f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394280"
---
# <span data-ttu-id="492b5-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="492b5-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="492b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="492b5-102">SYNOPSIS</span></span>
<span data-ttu-id="492b5-103">Inaktiverar avancerad data säkerhet på en server.</span><span class="sxs-lookup"><span data-stu-id="492b5-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="492b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="492b5-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="492b5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="492b5-105">DESCRIPTION</span></span>
<span data-ttu-id="492b5-106">Cmdleten **disable-AzSqlServerAdvancedDataSecurity** inaktiverar avancerad data säkerhet på en server.</span><span class="sxs-lookup"><span data-stu-id="492b5-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="492b5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="492b5-107">EXAMPLES</span></span>

### <span data-ttu-id="492b5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="492b5-108">Example 1</span></span>
### <span data-ttu-id="492b5-109">Exempel 2: inaktivera avancerad data säkerhet för servrar</span><span class="sxs-lookup"><span data-stu-id="492b5-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="492b5-110">Exempel 3: inaktivera avancerad data säkerhet för servrar från Server resurs</span><span class="sxs-lookup"><span data-stu-id="492b5-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="492b5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="492b5-111">PARAMETERS</span></span>

### <span data-ttu-id="492b5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="492b5-112">-DefaultProfile</span></span>
<span data-ttu-id="492b5-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="492b5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="492b5-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="492b5-114">-InputObject</span></span>
<span data-ttu-id="492b5-115">Serverobjektet som ska användas med avancerad data säkerhets policy åtgärd</span><span class="sxs-lookup"><span data-stu-id="492b5-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="492b5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="492b5-116">-ResourceGroupName</span></span>
<span data-ttu-id="492b5-117">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="492b5-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="492b5-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="492b5-118">-ServerName</span></span>
<span data-ttu-id="492b5-119">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="492b5-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="492b5-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="492b5-120">-Confirm</span></span>
<span data-ttu-id="492b5-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="492b5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="492b5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="492b5-122">-WhatIf</span></span>
<span data-ttu-id="492b5-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="492b5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="492b5-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="492b5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="492b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492b5-125">CommonParameters</span></span>
<span data-ttu-id="492b5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="492b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492b5-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="492b5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492b5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="492b5-128">INPUTS</span></span>

### <span data-ttu-id="492b5-129">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="492b5-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="492b5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="492b5-130">System.String</span></span>

## <span data-ttu-id="492b5-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="492b5-131">OUTPUTS</span></span>

### <span data-ttu-id="492b5-132">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="492b5-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="492b5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="492b5-133">NOTES</span></span>

## <span data-ttu-id="492b5-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="492b5-134">RELATED LINKS</span></span>
