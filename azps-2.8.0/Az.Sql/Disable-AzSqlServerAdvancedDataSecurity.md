---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: ca3b39ac369900f19c41b27b50efb06af7cf2056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920234"
---
# <span data-ttu-id="5c475-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="5c475-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="5c475-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c475-102">SYNOPSIS</span></span>
<span data-ttu-id="5c475-103">Inaktiverar avancerad data säkerhet på en server.</span><span class="sxs-lookup"><span data-stu-id="5c475-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="5c475-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c475-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c475-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c475-105">DESCRIPTION</span></span>
<span data-ttu-id="5c475-106">Cmdleten **disable-AzSqlServerAdvancedDataSecurity** inaktiverar avancerad data säkerhet på en server.</span><span class="sxs-lookup"><span data-stu-id="5c475-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="5c475-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c475-107">EXAMPLES</span></span>

### <span data-ttu-id="5c475-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5c475-108">Example 1</span></span>
### <span data-ttu-id="5c475-109">Exempel 1 – inaktivera avancerad data säkerhet för servrar</span><span class="sxs-lookup"><span data-stu-id="5c475-109">Example 1 - Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="5c475-110">Exempel 2 – inaktivera avancerad data säkerhet för servrar från Server resurs</span><span class="sxs-lookup"><span data-stu-id="5c475-110">Example 2 - Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="5c475-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c475-111">PARAMETERS</span></span>

### <span data-ttu-id="5c475-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c475-112">-DefaultProfile</span></span>
<span data-ttu-id="5c475-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c475-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c475-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c475-114">-InputObject</span></span>
<span data-ttu-id="5c475-115">Serverobjektet som ska användas med avancerad data säkerhets policy åtgärd</span><span class="sxs-lookup"><span data-stu-id="5c475-115">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c475-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c475-116">-ResourceGroupName</span></span>
<span data-ttu-id="5c475-117">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5c475-117">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c475-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c475-118">-ServerName</span></span>
<span data-ttu-id="5c475-119">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="5c475-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="5c475-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5c475-120">-Confirm</span></span>
<span data-ttu-id="5c475-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c475-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c475-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c475-122">-WhatIf</span></span>
<span data-ttu-id="5c475-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5c475-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c475-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5c475-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c475-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c475-125">CommonParameters</span></span>
<span data-ttu-id="5c475-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c475-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5c475-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c475-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c475-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c475-128">INPUTS</span></span>

### <span data-ttu-id="5c475-129">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5c475-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="5c475-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5c475-130">System.String</span></span>

## <span data-ttu-id="5c475-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c475-131">OUTPUTS</span></span>

### <span data-ttu-id="5c475-132">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5c475-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="5c475-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c475-133">NOTES</span></span>

## <span data-ttu-id="5c475-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c475-134">RELATED LINKS</span></span>
