---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f3492b0f6eb83f2c4a37a6fa073e7f579208cf62
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259084"
---
# <span data-ttu-id="63a38-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="63a38-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="63a38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63a38-102">SYNOPSIS</span></span>
<span data-ttu-id="63a38-103">Hämtar information om en Azure AD-administratör för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="63a38-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="63a38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63a38-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63a38-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63a38-105">DESCRIPTION</span></span>
<span data-ttu-id="63a38-106">Cmdleten **Get-AzSqlServerActiveDirectoryAdministrator** hämtar information om en Azure Active Directory (Azure AD-administratör) för en AzureSQL-server i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="63a38-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="63a38-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63a38-107">EXAMPLES</span></span>

### <span data-ttu-id="63a38-108">Exempel 1: hämtar information om en administratör för en server</span><span class="sxs-lookup"><span data-stu-id="63a38-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="63a38-109">Med det här kommandot får du information om en Azure AD-administratör för en server med namnet Server01 som är kopplad till en resurs grupp med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="63a38-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="63a38-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63a38-110">PARAMETERS</span></span>

### <span data-ttu-id="63a38-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a38-111">-DefaultProfile</span></span>
<span data-ttu-id="63a38-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="63a38-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63a38-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63a38-113">-ResourceGroupName</span></span>
<span data-ttu-id="63a38-114">Anger namnet på den resurs grupp som SQL-servern har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="63a38-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="63a38-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="63a38-115">-ServerName</span></span>
<span data-ttu-id="63a38-116">Anger namnet på den SQL Server som den här cmdleten får information om.</span><span class="sxs-lookup"><span data-stu-id="63a38-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a38-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63a38-117">-Confirm</span></span>
<span data-ttu-id="63a38-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63a38-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63a38-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63a38-119">-WhatIf</span></span>
<span data-ttu-id="63a38-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63a38-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63a38-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63a38-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63a38-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a38-122">CommonParameters</span></span>
<span data-ttu-id="63a38-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63a38-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a38-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63a38-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a38-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63a38-125">INPUTS</span></span>

### <span data-ttu-id="63a38-126">System. String</span><span class="sxs-lookup"><span data-stu-id="63a38-126">System.String</span></span>

## <span data-ttu-id="63a38-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63a38-127">OUTPUTS</span></span>

### <span data-ttu-id="63a38-128">Microsoft. Azure. commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="63a38-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="63a38-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63a38-129">NOTES</span></span>

## <span data-ttu-id="63a38-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63a38-130">RELATED LINKS</span></span>

[<span data-ttu-id="63a38-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="63a38-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="63a38-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="63a38-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="63a38-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="63a38-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="63a38-134">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="63a38-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


