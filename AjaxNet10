using Microsoft.AspNetCore.Html;
using Microsoft.AspNetCore.Http.Extensions;
using Microsoft.AspNetCore.Mvc;
using Microsoft.AspNetCore.Mvc.Rendering;
using Microsoft.AspNetCore.Mvc.Routing;
using Microsoft.AspNetCore.Mvc.ViewFeatures;
using System.Text.Encodings.Web;

namespace JqueryProva.Helpers
{
    /// <summary>
    /// AjaxNet10 - Replicazione completa helper AJAX MVC5 per ASP.NET Core
    /// Supporta tutti i metodi HTTP: GET, POST, PUT, DELETE, PATCH, HEAD, OPTIONS, TRACE
    /// </summary>
    public static class AjaxNet10
    {
        #region AjaxOptions (Identico MVC5)
        public class AjaxOptions
        {
            public string HttpMethod { get; set; } = "GET";
            public string UpdateTargetId { get; set; }
            public InsertionMode InsertionMode { get; set; } = InsertionMode.Replace;
            public string Confirm { get; set; }
            public string OnBegin { get; set; }
            public string OnComplete { get; set; }
            public string OnFailure { get; set; }
            public string OnSuccess { get; set; }
            public string LoadingElementId { get; set; }
            public int LoadingElementDuration { get; set; }
            public bool AllowCache { get; set; }
            public string Url { get; set; }
        }

        public enum InsertionMode
        {
            Replace,
            InsertBefore,
            InsertAfter,
            ReplaceWith
        }
        #endregion

        #region === ACTIONLINK COMPLETO (12 overload) ===

        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            AjaxOptions ajaxOptions)
        {
            return ActionLink(html, linkText, actionName, null, null, null, ajaxOptions, null);
        }

        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            object routeValues,
            AjaxOptions ajaxOptions)
        {
            return ActionLink(html, linkText, actionName, null, routeValues, null, ajaxOptions, null);
        }

        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            AjaxOptions ajaxOptions,
            object htmlAttributes)
        {
            return ActionLink(html, linkText, actionName, null, null, null, ajaxOptions, htmlAttributes);
        }

        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            RouteValueDictionary routeValues,
            AjaxOptions ajaxOptions)
        {
            return ActionLink(html, linkText, actionName, null, routeValues, null, ajaxOptions, null);
        }

        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            object routeValues,
            AjaxOptions ajaxOptions,
            object htmlAttributes)
        {
            return ActionLink(html, linkText, actionName, null, routeValues, null, ajaxOptions, htmlAttributes);
        }

        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            RouteValueDictionary routeValues,
            AjaxOptions ajaxOptions,
            IDictionary<string, object> htmlAttributes)
        {
            return ActionLink(html, linkText, actionName, null, routeValues, null, ajaxOptions, htmlAttributes);
        }

        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            string controllerName,
            AjaxOptions ajaxOptions)
        {
            return ActionLink(html, linkText, actionName, controllerName, null, null, ajaxOptions, null);
        }

        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            string controllerName,
            object routeValues,
            AjaxOptions ajaxOptions)
        {
            return ActionLink(html, linkText, actionName, controllerName, routeValues, null, ajaxOptions, null);
        }

        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            string controllerName,
            AjaxOptions ajaxOptions,
            object htmlAttributes)
        {
            return ActionLink(html, linkText, actionName, controllerName, null, null, ajaxOptions, htmlAttributes);
        }

        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            string controllerName,
            RouteValueDictionary routeValues,
            AjaxOptions ajaxOptions)
        {
            return ActionLink(html, linkText, actionName, controllerName, routeValues, null, ajaxOptions, null);
        }

        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            string controllerName,
            object routeValues,
            AjaxOptions ajaxOptions,
            object htmlAttributes)
        {
            return ActionLink(html, linkText, actionName, controllerName, routeValues, null, ajaxOptions, htmlAttributes);
        }

        // 🔴 CORRETTO: usa html.Url invece di GetRequiredService
        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            string controllerName,
            object routeValues,
            string protocol,
            AjaxOptions ajaxOptions,
            object htmlAttributes)
        {
            var urlHelper = GetUrlHelper(html);
            var url = urlHelper.Action(actionName, controllerName, routeValues, protocol);
            return GenerateLink(html, linkText, url, ajaxOptions, htmlAttributes);
        }

        // 🔴 CORRETTO: usa html.Url invece di GetRequiredService
        public static IHtmlContent ActionLink(
            this IHtmlHelper html,
            string linkText,
            string actionName,
            string controllerName,
            RouteValueDictionary routeValues,
            string protocol,
            string hostName,
            string fragment,
            AjaxOptions ajaxOptions,
            IDictionary<string, object> htmlAttributes)
        {
            var urlHelper = GetUrlHelper(html);
            var url = urlHelper.Action(actionName, controllerName, routeValues, protocol, hostName, fragment);
            return GenerateLink(html, linkText, url, ajaxOptions, htmlAttributes);
        }

        #endregion

        #region === BEGINFORM COMPLETO (15 overload) ===

        public static MvcForm BeginForm(this IHtmlHelper html, AjaxOptions ajaxOptions)
        {
            return BeginForm(html, null, null, null, null, ajaxOptions, null);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, AjaxOptions ajaxOptions)
        {
            return BeginForm(html, actionName, null, null, null, ajaxOptions, null);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, string controllerName, AjaxOptions ajaxOptions)
        {
            return BeginForm(html, actionName, controllerName, null, null, ajaxOptions, null);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, object routeValues, AjaxOptions ajaxOptions)
        {
            return BeginForm(html, actionName, null, routeValues, null, ajaxOptions, null);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, AjaxOptions ajaxOptions, object htmlAttributes)
        {
            return BeginForm(html, actionName, null, null, null, ajaxOptions, htmlAttributes);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, string controllerName, string httpMethod, AjaxOptions ajaxOptions)
        {
            return BeginForm(html, actionName, controllerName, null, httpMethod, ajaxOptions, null);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, string controllerName, AjaxOptions ajaxOptions, object htmlAttributes)
        {
            return BeginForm(html, actionName, controllerName, null, null, ajaxOptions, htmlAttributes);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, object routeValues, string httpMethod, AjaxOptions ajaxOptions)
        {
            return BeginForm(html, actionName, null, routeValues, httpMethod, ajaxOptions, null);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, object routeValues, AjaxOptions ajaxOptions, object htmlAttributes)
        {
            return BeginForm(html, actionName, null, routeValues, null, ajaxOptions, htmlAttributes);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, string controllerName, object routeValues, string httpMethod, AjaxOptions ajaxOptions)
        {
            return BeginForm(html, actionName, controllerName, routeValues, httpMethod, ajaxOptions, null);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, string controllerName, object routeValues, AjaxOptions ajaxOptions, object htmlAttributes)
        {
            return BeginForm(html, actionName, controllerName, routeValues, null, ajaxOptions, htmlAttributes);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, string controllerName, string httpMethod, AjaxOptions ajaxOptions, object htmlAttributes)
        {
            return BeginForm(html, actionName, controllerName, null, httpMethod, ajaxOptions, htmlAttributes);
        }

        public static MvcForm BeginForm(this IHtmlHelper html, string actionName, object routeValues, string httpMethod, AjaxOptions ajaxOptions, object htmlAttributes)
        {
            return BeginForm(html, actionName, null, routeValues, httpMethod, ajaxOptions, htmlAttributes);
        }
        private static IUrlHelper GetUrlHelper(IHtmlHelper html)
        {
            var urlHelperFactory = html.ViewContext.HttpContext.RequestServices.GetRequiredService<IUrlHelperFactory>();
            return urlHelperFactory.GetUrlHelper(html.ViewContext);
        }
        // 🔴 CORRETTO: usa html.Url invece di GetRequiredService
        public static MvcForm BeginForm(
            this IHtmlHelper html,
            string actionName,
            string controllerName,
            object routeValues,
            string httpMethod,
            AjaxOptions ajaxOptions,
            object htmlAttributes)
        {
            var urlHelper = GetUrlHelper(html);
            var url = urlHelper.Action(actionName, controllerName, routeValues);
            var method = httpMethod ?? ajaxOptions?.HttpMethod ?? "GET";
            return GenerateForm(html, url, method, ajaxOptions, htmlAttributes);
        }

        // 🔴 CORRETTO: usa html.Url invece di GetRequiredService
        public static MvcForm BeginForm(
            this IHtmlHelper html,
            string actionName,
            string controllerName,
            RouteValueDictionary routeValues,
            string httpMethod,
            AjaxOptions ajaxOptions,
            IDictionary<string, object> htmlAttributes)
        {
            var urlHelper = GetUrlHelper(html);
            var url = urlHelper.Action(actionName, controllerName, routeValues);
            var method = httpMethod ?? ajaxOptions?.HttpMethod ?? "GET";
            return GenerateForm(html, url, method, ajaxOptions, htmlAttributes);
        }

        #endregion

        #region === ROUTELINK COMPLETO (8 overload) ===

        public static IHtmlContent RouteLink(this IHtmlHelper html, string linkText, string routeName, AjaxOptions ajaxOptions)
        {
            return RouteLink(html, linkText, routeName, null, null, null, ajaxOptions, null);
        }

        public static IHtmlContent RouteLink(this IHtmlHelper html, string linkText, string routeName, object routeValues, AjaxOptions ajaxOptions)
        {
            return RouteLink(html, linkText, routeName, routeValues, null, null, ajaxOptions, null);
        }

        public static IHtmlContent RouteLink(this IHtmlHelper html, string linkText, string routeName, AjaxOptions ajaxOptions, object htmlAttributes)
        {
            return RouteLink(html, linkText, routeName, null, null, null, ajaxOptions, htmlAttributes);
        }

        public static IHtmlContent RouteLink(this IHtmlHelper html, string linkText, string routeName, RouteValueDictionary routeValues, AjaxOptions ajaxOptions)
        {
            return RouteLink(html, linkText, routeName, routeValues, null, null, ajaxOptions, null);
        }

        public static IHtmlContent RouteLink(this IHtmlHelper html, string linkText, string routeName, object routeValues, AjaxOptions ajaxOptions, object htmlAttributes)
        {
            return RouteLink(html, linkText, routeName, routeValues, null, null, ajaxOptions, htmlAttributes);
        }

        public static IHtmlContent RouteLink(this IHtmlHelper html, string linkText, string routeName, RouteValueDictionary routeValues, AjaxOptions ajaxOptions, IDictionary<string, object> htmlAttributes)
        {
            return RouteLink(html, linkText, routeName, routeValues, null, null, ajaxOptions, htmlAttributes);
        }

        // 🔴 CORRETTO: usa html.Url invece di GetRequiredService
        public static IHtmlContent RouteLink(
            this IHtmlHelper html,
            string linkText,
            string routeName,
            object routeValues,
            string protocol,
            string hostName,
            AjaxOptions ajaxOptions,
            object htmlAttributes)
        {

            var urlHelper = GetUrlHelper(html);
            var url = urlHelper.RouteUrl(routeName, routeValues, protocol, hostName);
            return GenerateLink(html, linkText, url, ajaxOptions, htmlAttributes);
        }

        // 🔴 CORRETTO: usa html.Url invece di GetRequiredService
        public static IHtmlContent RouteLink(
            this IHtmlHelper html,
            string linkText,
            string routeName,
            RouteValueDictionary routeValues,
            string protocol,
            string hostName,
            string fragment,
            AjaxOptions ajaxOptions,
            IDictionary<string, object> htmlAttributes)
        {

            var urlHelper = GetUrlHelper(html);
            var url = urlHelper.RouteUrl(new UrlRouteContext
            {
                RouteName = routeName,
                Values = routeValues,
                Protocol = protocol,
                Host = hostName,
                Fragment = fragment
            });
            return GenerateLink(html, linkText, url, ajaxOptions, htmlAttributes);
        }

        #endregion

        #region === BEGINROUTE FORM COMPLETO (6 overload) ===

        public static MvcForm BeginRouteForm(this IHtmlHelper html, string routeName, AjaxOptions ajaxOptions)
        {
            return BeginRouteForm(html, routeName, null, null, ajaxOptions, null);
        }

        public static MvcForm BeginRouteForm(this IHtmlHelper html, string routeName, object routeValues, AjaxOptions ajaxOptions)
        {
            return BeginRouteForm(html, routeName, routeValues, null, ajaxOptions, null);
        }

        public static MvcForm BeginRouteForm(this IHtmlHelper html, string routeName, AjaxOptions ajaxOptions, object htmlAttributes)
        {
            return BeginRouteForm(html, routeName, null, null, ajaxOptions, htmlAttributes);
        }

        public static MvcForm BeginRouteForm(this IHtmlHelper html, string routeName, RouteValueDictionary routeValues, AjaxOptions ajaxOptions)
        {
            return BeginRouteForm(html, routeName, routeValues, null, ajaxOptions, null);
        }

        public static MvcForm BeginRouteForm(this IHtmlHelper html, string routeName, object routeValues, string httpMethod, AjaxOptions ajaxOptions)
        {
            return BeginRouteForm(html, routeName, routeValues, httpMethod, ajaxOptions, null);
        }

        // 🔴 CORRETTO: usa html.Url invece di GetRequiredService
        public static MvcForm BeginRouteForm(this IHtmlHelper html, string routeName, RouteValueDictionary routeValues, string httpMethod, AjaxOptions ajaxOptions, IDictionary<string, object> htmlAttributes)
        {
            var urlHelper = GetUrlHelper(html);
            var url = urlHelper.RouteUrl(routeName, routeValues);
            var method = httpMethod ?? ajaxOptions?.HttpMethod ?? "GET";
            return GenerateForm(html, url, method, ajaxOptions, htmlAttributes);
        }

        // 🔴 CORRETTO: usa html.Url invece di GetRequiredService
        public static MvcForm BeginRouteForm(this IHtmlHelper html, string routeName, object routeValues, string httpMethod, AjaxOptions ajaxOptions, object htmlAttributes)
        {
            var urlHelper = GetUrlHelper(html);
            var url = urlHelper.RouteUrl(routeName, routeValues);
            var method = httpMethod ?? ajaxOptions?.HttpMethod ?? "GET";
            return GenerateForm(html, url, method, ajaxOptions, htmlAttributes);
        }

        #endregion

        #region === UTILITY AGGIUNTIVE ===

        public static IHtmlContent AjaxPanel(
            this IHtmlHelper html,
            string panelId,
            string updateUrl,
            string initialContent = null,
            object htmlAttributes = null)
        {
            var tag = new TagBuilder("div");
            tag.Attributes["id"] = panelId;
            tag.Attributes["data-ajax-url"] = updateUrl;
            tag.Attributes["data-ajax-panel"] = "true";

            if (htmlAttributes != null)
            {
                var attrs = HtmlHelper.AnonymousObjectToHtmlAttributes(htmlAttributes);
                tag.MergeAttributes(attrs);
            }

            if (!string.IsNullOrEmpty(initialContent))
            {
                tag.InnerHtml.AppendHtml(initialContent);
            }

            var writer = new StringWriter();
            tag.WriteTo(writer, HtmlEncoder.Default);
            return new HtmlString(writer.ToString());
        }

        public static IHtmlContent AutoRefreshPanel(
            this IHtmlHelper html,
            string panelId,
            string updateUrl,
            int intervalMilliseconds = 5000,
            string loadingMessage = "Caricamento...")
        {
            var script = $@"
                <div id='{panelId}' data-refresh-url='{updateUrl}' data-refresh-interval='{intervalMilliseconds}'>
                    <span class='loading'>{loadingMessage}</span>
                </div>
                <script>
                    (function() {{
                        var panel = document.getElementById('{panelId}');
                        var url = panel.getAttribute('data-refresh-url');
                        var interval = parseInt(panel.getAttribute('data-refresh-interval'));
                        
                        function refresh() {{
                            fetch(url)
                                .then(r => r.text())
                                .then(html => panel.innerHTML = html)
                                .catch(e => console.error('Refresh error:', e));
                        }}
                        
                        refresh();
                        setInterval(refresh, interval);
                    }})();
                </script>";

            return new HtmlString(script);
        }

        public static IHtmlContent ActionImageLink(
            this IHtmlHelper html,
            string imageUrl,
            string altText,
            string actionName,
            string controllerName,
            AjaxOptions ajaxOptions,
            object htmlAttributes = null)
        {
            var imgTag = new TagBuilder("img");
            imgTag.Attributes["src"] = imageUrl;
            imgTag.Attributes["alt"] = altText;

            var imgHtml = new StringWriter();
            imgTag.WriteTo(imgHtml, HtmlEncoder.Default);

            return ActionLink(html, imgHtml.ToString(), actionName, controllerName, ajaxOptions, htmlAttributes);
        }

        #endregion

        #region === GENERATORI PRIVATI ===

        private static IHtmlContent GenerateLink(
            IHtmlHelper html,
            string linkText,
            string url,
            AjaxOptions ajaxOptions,
            object htmlAttributes)
        {
            var tag = new TagBuilder("a");
            tag.Attributes["href"] = url;
            tag.InnerHtml.AppendHtml(linkText);

            // ATTENZIONE: Questa riga è fondamentale!
            tag.Attributes["data-ajax"] = "true";

            ApplyAjaxAttributes(tag, ajaxOptions);

            if (htmlAttributes != null)
            {
                var attrs = HtmlHelper.AnonymousObjectToHtmlAttributes(htmlAttributes);
                tag.MergeAttributes(attrs);
            }

            var writer = new StringWriter();
            tag.WriteTo(writer, HtmlEncoder.Default);
            return new HtmlString(writer.ToString());
        }

        private static MvcForm GenerateForm(
            IHtmlHelper html,
            string url,
            string httpMethod,
            AjaxOptions ajaxOptions,
            object htmlAttributes)
        {
            var tag = new TagBuilder("form");
            tag.Attributes["action"] = url;

            var method = (httpMethod ?? "GET").ToUpperInvariant();
            tag.Attributes["method"] = (method == "GET") ? "GET" : "POST";
            tag.Attributes["data-ajax"] = "true";
            tag.Attributes["data-ajax-method"] = method;

            ApplyAjaxAttributes(tag, ajaxOptions);

            if (htmlAttributes != null)
            {
                var attrs = HtmlHelper.AnonymousObjectToHtmlAttributes(htmlAttributes);
                tag.MergeAttributes(attrs);
            }

            var writer = new StringWriter();
            tag.WriteTo(writer, HtmlEncoder.Default);
            html.ViewContext.Writer.Write(writer.ToString());

            return new MvcForm(html.ViewContext);
        }

        private static void ApplyAjaxAttributes(TagBuilder tag, AjaxOptions options)
        {
            if (options == null) return;

            if (!string.IsNullOrEmpty(options.HttpMethod))
                tag.Attributes["data-ajax-method"] = options.HttpMethod.ToUpperInvariant();

            if (!string.IsNullOrEmpty(options.UpdateTargetId))
                tag.Attributes["data-ajax-update"] = "#" + options.UpdateTargetId;

            if (!string.IsNullOrEmpty(options.Confirm))
                tag.Attributes["data-ajax-confirm"] = options.Confirm;

            if (!string.IsNullOrEmpty(options.OnBegin))
                tag.Attributes["data-ajax-begin"] = options.OnBegin;

            if (!string.IsNullOrEmpty(options.OnComplete))
                tag.Attributes["data-ajax-complete"] = options.OnComplete;

            if (!string.IsNullOrEmpty(options.OnFailure))
                tag.Attributes["data-ajax-failure"] = options.OnFailure;

            if (!string.IsNullOrEmpty(options.OnSuccess))
                tag.Attributes["data-ajax-success"] = options.OnSuccess;

            if (!string.IsNullOrEmpty(options.LoadingElementId))
                tag.Attributes["data-ajax-loading"] = "#" + options.LoadingElementId;

            if (!string.IsNullOrEmpty(options.Url))
                tag.Attributes["data-ajax-url"] = options.Url;

            var mode = options.InsertionMode switch
            {
                InsertionMode.Replace => "REPLACE",
                InsertionMode.InsertBefore => "BEFORE",
                InsertionMode.InsertAfter => "AFTER",
                InsertionMode.ReplaceWith => "REPLACEMENT",
                _ => "REPLACE"
            };
            tag.Attributes["data-ajax-mode"] = mode;

            if (options.AllowCache)
                tag.Attributes["data-ajax-cache"] = "true";

            if (options.LoadingElementDuration > 0)
                tag.Attributes["data-ajax-loading-duration"] = options.LoadingElementDuration.ToString();
        }

        #endregion
    }

    #region === MvcForm ===

    public class MvcForm : IDisposable
    {
        private readonly ViewContext _viewContext;
        private bool _disposed;

        public MvcForm(ViewContext viewContext)
        {
            _viewContext = viewContext ?? throw new ArgumentNullException(nameof(viewContext));
        }

        public void Dispose()
        {
            if (!_disposed)
            {
                _viewContext.Writer.Write("</form>");
                _disposed = true;
            }
        }
    }

    #endregion

    #region === ESTENSIONI AGGIUNTIVE ===

    public static class AjaxNet10Extensions
    {
        public static IHtmlContent AjaxSubmitButton(
            this IHtmlHelper html,
            string buttonText,
            object htmlAttributes = null)
        {
            var tag = new TagBuilder("button");
            tag.Attributes["type"] = "submit";
            tag.InnerHtml.Append(buttonText);

            if (htmlAttributes != null)
            {
                var attrs = HtmlHelper.AnonymousObjectToHtmlAttributes(htmlAttributes);
                tag.MergeAttributes(attrs);
            }

            var writer = new StringWriter();
            tag.WriteTo(writer, HtmlEncoder.Default);
            return new HtmlString(writer.ToString());
        }

        public static IHtmlContent AjaxLoading(
            this IHtmlHelper html,
            string elementId,
            string message = "Caricamento in corso...")
        {
            return new HtmlString(
                $"<div id=\"{elementId}\" style=\"display:none;\" class=\"ajax-loading\">{message}</div>");
        }

        public static IHtmlContent AjaxScripts(this IHtmlHelper html)
        {
            return new HtmlString(@"
                <script src=""https://code.jquery.com/jquery-3.6.0.min.js""></script>
                <script src=""https://cdn.jsdelivr.net/npm/jquery-ajax-unobtrusive@3.2.6/dist/jquery.unobtrusive-ajax.min.js""></script>");
        }
    }

    #endregion
}